# Requirements: Conductor

## 1. Problem statement
AI agents should create value, not operational headaches. Teams now run agents built on many platforms, and nobody can see which ones exist, what they cost, which are risky, or who approved what. IBM watsonx Orchestrate exists to build, deploy, orchestrate, manage and govern agents wherever they are built or run. Conductor is a working prototype of that control desk.

## 2. Users
- **Operations lead:** wants one view of every agent and its net value.
- **Risk or compliance owner:** wants approvals for risky actions and an audit trail.
- **Finance owner:** wants spend caps per agent.

## 3. Functional requirements
| ID | Requirement | Acceptance check |
|----|-------------|------------------|
| FR-1 | Registry lists agents from any platform with skill, risk, net value and status | Table shows 5 agents with origin column |
| FR-2 | User can pause and resume an agent | Paused agent never receives routed work |
| FR-3 | Orchestrator routes a task to the active agent with the highest net value for that skill | Test: route picks highest net value |
| FR-4 | Spend cap blocks a task that would exceed the per-agent monthly limit | Test: decide blocks over cap |
| FR-5 | Tasks at or above the chosen risk level wait in an approval queue | Test: high risk becomes pending |
| FR-6 | Approve or reject updates spend and the audit trail | Log entry appears for each decision |
| FR-7 | Every route, pause, resume, approval and rejection is logged with time | Audit trail shows newest first |
| FR-8 | Built-in self-tests run from the page | 15 of 15 tests pass |
| FR-9 | A 3-minute demo script is included (readme.md and the page) | Script covers hook, problem, demo, technical, innovation, closing |

## 4. Non-functional requirements
**Security**
- Content Security Policy blocks all network access, remote scripts and form posts.
- No `innerHTML`, `eval` or inline event attributes. All user text is written with `textContent`.
- Input is length-limited, stripped of control characters and angle brackets, and range-validated.
- No data leaves the browser and nothing is stored.

**Accessibility (WCAG 2.2 AA target)**
- Skip link, landmarks, one `h1`, ordered headings, table caption and row headers.
- Every control has a visible label; buttons have descriptive accessible names.
- Live regions announce queue, log and test results; errors use `role="alert"`.
- 44 px minimum targets, visible focus ring, contrast of at least 4.5:1, reduced-motion respected, works at 200% zoom.

**Efficiency**
- One file, under 20 KB, zero dependencies, zero requests.
- Rendering uses `replaceChildren`; the audit trail is capped at 50 entries.

**Code quality**
- Pure functions (`route`, `decide`, `validate`, `sanitize`, `netValue`) separated from DOM code.
- Strict mode, no globals beyond state, consistent naming.

## 5. Out of scope
Real agent execution, authentication and persistent storage. These belong to the production platform.

## 6. Success criteria
All FR checks pass, self-tests report 15 of 15, keyboard-only use completes every flow, and a screen reader announces every state change.
