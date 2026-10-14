# TutorX Architecture

## Current architecture

TutorX is a static single-page learning application in the root `index.html`. It uses plain HTML, CSS and JavaScript, with no bundler, framework, runtime server, or external API requirement. GitHub Pages can serve the file directly.

## Runtime components

- **View navigation:** switches between dashboard, curriculum, lesson studio, flashcards, challenge lab, subnetting trainer, interview prep, progress, glossary and study guide.
- **Curriculum data:** a JavaScript data structure stores section metadata, lesson bodies, concept points, flashcards and quiz questions.
- **Learning engine:** renders lessons, scores quiz responses, displays explanations, grants XP and unlocks achievements.
- **Flashcard engine:** filters cards by section, flips answers, marks cards as known and tracks cards for review.
- **Subnet calculator:** converts IPv4 dotted-decimal addresses to unsigned 32-bit values, applies a CIDR mask, calculates network/broadcast boundaries and shows host counts. /31 and /32 receive special treatment.
- **Scenario engine:** presents a simulated customer issue, multiple possible next actions and an explanation.
- **Interview engine:** filters questions, expands model answer frameworks and offers a local text area for practice.
- **Progress store:** saves learning state to `localStorage` under the versioned key `tutorx-state-v1`.
- **Search and glossary:** local search over the curriculum and a static networking glossary.

## State model

The saved state contains XP, completed lesson keys, quiz results, known/review cards, earned badges, study streak metadata, theme preference, daily tasks, quiz history, visited sections, active section and flashcard position.

All persistent data is local to the browser profile. It is not synchronized between devices or uploaded to a server. Export a JSON backup before clearing site data.

## Security and privacy

- No login or personal-data collection is required.
- No API keys or secrets should be placed in this static repository.
- Learner notes typed into interview practice are not uploaded by the application.
- Do not add analytics, remote fonts, external scripts, or tracking without a documented privacy review.
- Avoid rendering learner-provided strings as raw HTML if user-generated content is added in a future release. Use `textContent` or a well-reviewed sanitizer.
- Use only authorized lab environments for any future command or network simulation features.

## Accessibility

- Use semantic headings, labels, buttons and navigation landmarks.
- Preserve keyboard operation for controls and the flashcard flip interaction.
- Maintain visible focus indicators and sufficient contrast.
- Respect `prefers-reduced-motion`.
- Provide explanatory text with color-coded feedback so color is not the only signal.
- Test narrow screens and zoomed layouts.

## Known trade-offs

- A single HTML file is simple to deploy but makes large-scale content editing and automated testing harder.
- Progress is browser-local; private browsing, storage cleanup, or another device may not retain it.
- XP and quiz history are motivational signals, not a validated measure of professional competence.
- Content is authored and deterministic. It is not a live AI tutor and does not access real customer or provider networks.

## Suggested future structure

After the first release stabilizes, consider splitting the application into:

- `index.html` for the app shell.
- `src/styles.css` for design tokens and components.
- `src/app.js` for navigation and state.
- `src/data/curriculum.js` for lesson data.
- `src/data/questions.js` for assessments.
- `src/modules/subnetting.js` for IPv4 calculations.
- `tests/` for calculation, scoring and navigation checks.

Do not introduce a build system solely for its own sake. Adopt one when content size, tests, or component reuse justify it.