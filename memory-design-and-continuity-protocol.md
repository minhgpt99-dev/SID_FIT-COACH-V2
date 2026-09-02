# SID Fit Coach — Memory Design and Continuity Protocol

## 1. Decision

A knowledge file is **not** a live memory system. It is a static reference uploaded when the Custom GPT is configured. It is appropriate for stable instructions, training principles, response templates, safety rules, and the baseline design, but it cannot reliably record each new check-in, update a weekly trend, or retain operational facts across unrelated new chats.

A ChatGPT Custom GPT may have access to platform-level conversation context or user memory depending on product settings and availability, but this must be treated as a convenience layer, not the authoritative coaching record. The GPT must never claim a check-in was stored permanently unless the user explicitly sees it in the active thread or has copied it to an external record.

For a personal MVP that minimizes requests, the recommended design is **Conversation-Scoped Memory + Portable Memory Card**. It uses no external Actions, database, bot, or multi-step agent flow. One user message still produces one GPT response.

## 2. Memory architecture using SID

### L1 — Memory Framing

| Field | Decision |
|---|---|
| Memory problem | The coach must retain only the facts required to make safe, trend-aware decisions without pretending that a Custom GPT is a database |
| Primary user | One adult user in a single ongoing coaching conversation |
| What must persist in the active thread | Profile, current targets, program week, current training plan, recent check-ins, weekly trend, current behavior experiment, safety notes |
| What should not be retained as a running record | Full chat transcript, unnecessary personal data, raw meal-photo details, speculative health inferences |
| Transfer artifact | Portable Memory Card in YAML that the user can copy into a fresh chat |
| Quality target | The GPT can reconstruct a usable decision context in under 150–250 words/token-equivalent of structured data |

### L3 — Memory Decomposition

```text
Memory
├── Stable profile memory
│   ├── age/sex/height
│   ├── equipment and schedule
│   ├── goals and preferences
│   └── confirmed safety-relevant constraints
├── Active plan memory
│   ├── current program week/phase
│   ├── training schedule and progression rule
│   ├── current targets
│   └── current behavior experiment
├── Rolling evidence memory
│   ├── last 7 daily check-ins
│   ├── latest waist measure
│   ├── training completions and notable performance
│   └── sleep/steps/protein adherence summary
├── Decision memory
│   ├── latest weekly review
│   ├── why a plan change was or was not made
│   └── next review trigger
└── Safety memory
    ├── user-reported condition or medication if disclosed
    ├── injury/symptom status only while relevant
    └── escalation advice already given
```

### L4 — Memory schema

```yaml
sid_fit_coach_memory:
  memory_version: 1
  updated_on: YYYY-MM-DD
  stable_profile:
    age: 27
    sex: male
    height_cm: 168
    starting_weight_kg: 87
    equipment: full gym
    schedule: 3 core sessions + 1 optional
    goal: sustainable fat loss with strength/muscle retention
    reported_health_constraints: none reported
  active_plan:
    program_week: 1
    phase: foundation
    calories_target: 2150-2250 starting range
    protein_target_g: 140-160
    steps_target: 8000 starting target
    training_plan: 3 full-body sessions; optional recovery/cardio session
    current_experiment: establish 3 sessions and daily protein anchor
  rolling_evidence:
    weight_7d_average_kg: null
    waist_cm_latest: null
    training_last_7d: 0/3
    protein_days_near_target_last_7d: 0/7
    steps_7d_average: null
    sleep_7d_average_h: null
    important_notes: []
  latest_decision:
    date: YYYY-MM-DD
    assessment: insufficient data / maintain / adjust one variable
    rationale: no trend data yet
    next_review_when: after 7 check-ins or YYYY-MM-DD
  safety:
    active_flags: []
    note: no current red flags reported
```

## 3. Memory lifecycle

### 3.1 Start of a coaching thread

The GPT should confirm the stable profile already supplied in Knowledge, then ask only for material missing items. It should create an initial Memory Card once the user confirms those items.

### 3.2 Routine chat

Do not output the full Memory Card after every response. Read the active conversation for context, respond in one turn, and internally track the changes.

At the end of a check-in, show only this optional short footer if an important state changed:

```text
Memory update: đã ghi nhận [một thay đổi quan trọng] trong cuộc trò chuyện hiện tại.
```

Do not say that it was saved permanently.

### 3.3 Explicit memory commands

Recognize these Vietnamese commands:

| Command | Required behavior |
|---|---|
| `Lưu trạng thái` | Output the full portable Memory Card in YAML, based only on confirmed active-chat data |
| `Xem trạng thái` | Show a short human-readable dashboard, not necessarily YAML |
| `Cập nhật hồ sơ: ...` | Confirm the changed field, explain any plan impact, and regenerate Memory Card only if asked |
| `Review tuần` | Use the data supplied in thread; output a weekly review and update the decision fields in the next Memory Card if requested |
| `Khôi phục trạng thái` followed by YAML | Parse the card, identify conflicts/missing values, confirm the active context, and continue coaching |
| `Quên ...` | Confirm that the GPT will no longer use the named item in the current coaching context; explain platform-level memory cannot be guaranteed or altered by the GPT itself |

### 3.4 Weekly consolidation

After a weekly review, if the user has enough data, compress the detailed week into a Decision Memory:

- 7-day weight average and prior average;
- waist trend if supplied;
- training adherence;
- one or two blockers;
- one change or an explicit decision to maintain;
- next review date/trigger.

Do not repeat every meal or every message. This is the L8 synthesis step: raw logs become a reusable decision record.

## 4. Memory validation rules (L7)

Before outputting a Memory Card, apply these checks:

| Validation check | Rule |
|---|---|
| Fact integrity | Store only values explicitly supplied by user, calculated transparently from supplied values, or already confirmed in the active profile |
| Assumption exclusion | Do not store inferred food calories, diagnoses, or unconfirmed explanations as stable facts |
| Freshness | Include `updated_on`; mark old trend fields as `null` rather than treating stale values as current |
| Minimality | Keep only fields that will change coaching decisions |
| Conflict detection | If the user supplies a value contradicting the existing card, flag the conflict and ask one clarification question |
| Safety separation | Store safety-sensitive facts only when user explicitly gives them and they remain relevant; do not repeat sensitive details unnecessarily |
| Decision traceability | Every plan adjustment must have a short rationale tied to trend/adherence data |
| Portability | The complete YAML must fit in one easily copied code block |

## 5. Memory quality rubric

| Dimension | 0–1 | 2 | 3 |
|---|---|---|---|
| Profile integrity | Missing or invented facts | Basic profile but stale/unclear | Confirmed, minimal, and date-aware |
| Trend integrity | Snapshot treated as trend | Some averages but missing context | Trend, waist/performance/adherence and uncertainty aligned |
| Decision integrity | Unexplained change | Change has weak rationale | One-variable decision linked to evidence |
| Safety | Sensitive data treated casually | Basic warning | Explicit boundary, minimal retention, clear escalation |
| Portability | Too long/unstructured | Copyable but incomplete | Compact, self-contained, recoverable in a new chat |

A Memory Card must score at least 12/15 before being presented as the current coaching state.

## 6. Test suite

| Test | Input | Expected memory behavior |
|---|---|---|
| M01 | “Lưu trạng thái” after onboarding | Card contains profile and active plan; empty trend values remain null |
| M02 | User sends one scale weight | Card may record latest data but does not label it a 7-day trend |
| M03 | User has 7 weights and says “Review tuần” | Card contains calculated/supplied 7-day average and one decision |
| M04 | User reports a richer dinner | No moral label, no permanent negative “compliance” trait stored |
| M05 | User reports chest pain while running | Safety response first; if a card is requested, active safety flag is recorded only as user-reported context |
| M06 | New chat + pasted card | GPT recognizes it as portable memory, confirms key fields, and continues without full re-onboarding |
| M07 | Card says 87 kg but user says 82 kg current weight | GPT flags the mismatch as a current-data update, not an error or deception |
| M08 | User says “Quên cân nặng của tôi” | GPT stops using it in current thread and explains it cannot guarantee modification of platform-level settings |

## 7. Recommended user workflow: zero additional AI calls

1. Use one continuous chat for day-to-day coaching.
2. Send short check-ins in a consistent form, for example: `Check-in: 86.4 kg | tập A xong | 8.100 bước | ngủ 7h | protein gần đạt`.
3. Ask `Review tuần` once weekly; the GPT completes it in one response.
4. At the end of each weekly review, write `Lưu trạng thái`; the GPT returns one portable card in one response.
5. If starting a new chat, paste the card first and write `Khôi phục trạng thái`.

This is the most reliable no-code model with the fewest AI interactions. It does not rely on unverified platform memory, does not require Actions, and keeps memory artifacts auditable.

## 8. Upgrade path

If permanent, automatic, queryable memory later becomes a priority, add an external Action connected to a small database. The custom GPT would then need an Action call to read/write memory. This improves retention but no longer guarantees one request end-to-end because tool calls are part of the response loop.

For the present personal MVP, do not add this complexity. Use the Portable Memory Card until actual usage shows that manual weekly saving is a burden.

## 9. Confidence

High confidence: static Knowledge cannot function as dynamic operational memory; structured state and weekly consolidation improve reliability and align with SID's Frame → Architect → Validate → Synthesize → Transfer logic.

Medium confidence: any platform-managed Custom GPT memory behavior can vary by product plan, settings, workspace policy, and future product changes. Therefore the workflow must remain correct even when platform memory is unavailable.
