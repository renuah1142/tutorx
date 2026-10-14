# TutorX Product Plan

## Vision

TutorX is a responsive, browser-first learning game that prepares an aspiring CSC Tier 1 Engineer, B2B candidate for networking fundamentals, first-line troubleshooting, telecom service concepts, NOC operations, and technical interviews.

## Product goals

1. Turn a long study curriculum into short, approachable learning sessions.
2. Make retrieval practice the default through flashcards, quizzes, explanations, and scenarios.
3. Teach the reasoning process expected in Tier 1 support, not just terminology.
4. Make progress visible through lessons, XP, achievements, section completion, and practice history.
5. Keep the first release free to host and easy to maintain on GitHub Pages.
6. Avoid requiring an account, server, API key, or paid service for core learning features.

## Target learner

- Beginner or early-career IT / Computer Science graduate.
- Candidate preparing for a Tier 1 B2B support, NOC, service desk, or network support interview.
- Learner who benefits from simple definitions, practical analogies, repetition, and quizzes.

## Core user journeys

### First visit
1. Open the dashboard.
2. Understand the 11-section pathway.
3. Start Section 1, Networking Fundamentals.
4. Read a lesson, explain it back, and mark it complete.
5. Answer a section quiz and review explanations.
6. Use flashcards or a challenge to reinforce learning.

### Returning learner
1. Dashboard restores local progress.
2. Continue learning opens the first incomplete lesson.
3. Review cards and missed concepts.
4. Complete a quiz or scenario.
5. Review the progress report and export a backup.

### Interview practice
1. Filter technical, troubleshooting, or behavioural questions.
2. Attempt an answer before opening the model framework.
3. Use the mock interview prompt to practise speaking.
4. Review the readiness checklist and revisit weak sections.

## Release 1 feature scope

- Responsive dashboard and navigation.
- Eleven sections with lesson pages and concept cards.
- Flashcard arena with answer reveal, known-card tracking, and review marking.
- Scored quizzes with immediate feedback and explanations.
- Outage-detective scenarios based on plausible Tier 1 situations.
- IPv4 subnet calculator for prefixes /0 through /32, with special handling for /31 and /32.
- Interview question bank with model answer frameworks and optional local drafting.
- Searchable glossary.
- Local progress, XP, streak, badges, section completion, and JSON export/reset.
- Dark and light themes.
- GitHub Pages deployment workflow.
- Repository documentation for the product, curriculum, learning design, architecture, deployment, roadmap, and contribution standards.

## Non-goals for the first release

- No AI API or claim of generative tutoring. The initial tutor uses authored explanations, branching exercises, and deterministic feedback.
- No accounts, server database, cloud sync, leaderboards, or collection of learner data.
- No real network scanning, device login, packet injection, or production configuration changes.
- No claim that course completion guarantees a job, certification, or specific interview outcome.

## Design principles

- Calm, modern, readable UI with a clear hierarchy and limited visual noise.
- Mobile-first layouts and large touch targets.
- Every quiz response should teach, not just mark right or wrong.
- Use realistic B2B / NOC examples and distinguish confirmed evidence from hypotheses.
- Keep navigation predictable and state visible.
- Respect reduced-motion preferences and keyboard access.
- Store progress locally and explain that clearing browser storage removes it.

## Success criteria

- A learner can open the site without installing dependencies.
- The core experience works on current desktop and mobile browsers.
- Navigation, lesson completion, quizzes, flashcards, subnetting, scenarios, glossary, theme, progress export and reset work without a backend.
- Progress survives page refresh in the same browser.
- All lesson content and question banks are reviewable as plain source code.
- The site can deploy to GitHub Pages through a documented process.

## Risks and mitigations

| Risk | Mitigation |
|---|---|
| Learner memorizes answers without understanding | Include explanations, teach-back prompts, and scenario questions. |
| Progress disappears when browser data is cleared | Offer JSON export and explain local-only storage. |
| Networking edge cases are oversimplified | Add caveats, standards references, and review subnet edge cases. |
| Learner mistakes a practice answer for provider policy | State that actual SLA, access, and escalation rules come from the employer. |
| Static content grows hard to maintain | Keep a documented content schema and split curriculum into data files in a later phase if needed. |

## Future extensions

- Dedicated spaced-repetition scheduling for missed flashcards.
- Per-topic mastery and missed-question analytics.
- More extensive subnetting drills with step-by-step calculations.
- Interactive OSI packet journey and VLAN/routing diagrams.
- Additional troubleshooting branches with scoring rubrics.
- Optional import/export of progress and study plans.
- Optional AI tutor integration only after an explicit product, privacy, cost, and security decision.