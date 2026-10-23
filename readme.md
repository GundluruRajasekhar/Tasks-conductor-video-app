# Conductor: AI agent control desk

Built for the IBM watsonx Orchestrate challenge: *AI agents should create value, not operational headaches.*

Conductor shows how one control desk can **build visibility, orchestrate, manage and govern** agents from any platform.

## What it does
1. **Registry:** see every agent, where it runs, its risk and its net value per month. Pause or resume any agent.
2. **Orchestration:** send a task by skill. Conductor picks the active agent with the best net value.
3. **Governance:** a per-agent spend cap blocks overspend. Risky tasks wait for a human to approve or reject.
4. **Audit trail:** every decision is logged with a time.
5. **Self-tests:** one button runs 15 checks on the routing, policy and input rules.

## Run it
Open `index.html` in any modern browser. No install, no build, no network.

## How it maps to the problem statement
| Challenge theme | Feature |
|-----------------|---------|
| Wherever they are built or run | Origin column covers watsonx Orchestrate, Python, LangChain and SaaS agents |
| Orchestrate | Skill-based routing by net value |
| Manage | Pause, resume, spend caps, value metrics |
| Govern | Approval queue and audit trail |
| Value, not headaches | Net value is the headline number |

## Security
CSP with `default-src 'none'`, no `innerHTML` or `eval`, sanitised and range-checked input, no storage, no network.

## Accessibility
Skip link, landmarks, labelled controls, live regions, visible focus, 44 px targets, AA contrast, reduced motion.

## Tests
Press **Run self-tests** on the page. Expected: `15 of 15 tests passed.`

## Project files
`index.html` (app) · `requirements.md` · `readme.md` · `tasks.md`

## Next steps
Connect to the real watsonx Orchestrate APIs, add sign-in and role-based approvals, and persist the audit trail.

## Demo video script (3 minutes)

**0:00-0:15 Hook.** "Every day, teams lose time and money because AI agents are scattered across platforms, and nobody can see what they cost, what they are allowed to do, or who approved it. What if one conductor coordinated them all? Hi everyone, I'm Rajasekhar, and this is Conductor."

**0:15-0:45 Problem.** "I built an AI agent control desk that acts like a project manager for your agents. Teams face three problems: agent sprawl, overspending, and no accountability for risky actions. Managers cannot see the value and compliance teams cannot see the trail. Conductor solves this from one place."

**0:45-1:45 Demo (do live, slowly).**
1. Registry: "Every agent shows where it runs, its risk and its net value per month."
2. Send a Finance task at $20: "Conductor picks the active agent with the best net value, runs it and logs it."
3. Send an HR task: "This agent is high risk, so the task waits for a human." Click Approve.
4. Set the cap to 100 and send Finance again: "A spend cap stops the task before it costs more than allowed."
5. Send a Sales task: "That agent is paused, so Conductor refuses and says why."
6. Scroll to the audit trail: "Every decision is recorded with a time."

**1:45-2:20 Technical excellence.** Show the four files. "Logic is separate from the interface. Security comes from a strict content security policy, no unsafe code execution and validated input. It is one small file with no dependencies, built for keyboard and screen-reader use, with 15 built-in tests." Click Run self-tests and show "15 of 15 tests passed."

**2:20-2:45 Innovation.** "Conductor does not just list agents, it governs them. Next: real watsonx Orchestrate APIs, sign-in with role-based approvals, and a saved audit trail, making it an enterprise-ready control layer."

**2:45-3:00 Closing.** "Conductor turns agent chaos into value you can see, spend you can control and decisions you can audit. AI agents should create value, not operational headaches. Thank you."

### Recording tips
Speak slightly slower than normal and smile. Record at 1080p with the browser at 125% zoom and no other tabs. Add a 5-second title card with your name and "Conductor". Keep music at 10-15% under the voice. Practise the six demo clicks twice.
