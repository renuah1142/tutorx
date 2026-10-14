# Contributing and Content Standards

## Repository principles

- Keep the first-run experience simple and fast.
- Keep core learning features available without a backend.
- Do not commit API keys, passwords, tokens, customer data, private IP plans, or production configuration.
- Do not add dependencies without explaining the benefit and maintenance cost.
- Keep the app usable on mobile and keyboard-accessible.

## Lesson content template

Each new lesson should define:

- Section and lesson ID.
- Title and learning objective.
- Beginner-friendly explanation.
- Key terms with precise definitions.
- Practical B2B/NOC example.
- Memory aid or common misconception.
- One or more assessment questions.
- References for standards, vendor behavior or technical claims.

## Assessment content template

Each question should have a clear prompt, answer options when applicable, a single best answer, an explanation, and a link to the lesson or objective it tests. Avoid ambiguous distractors and unverified facts.

## UI checklist

- Does the screen work at narrow mobile widths?
- Are buttons and inputs keyboard accessible?
- Is focus visible?
- Does text meet contrast needs in both themes?
- Does feedback include words/icons rather than color alone?
- Are empty, invalid and completed states handled?
- Is user data stored locally explained accurately?
- Does reduced-motion preference remain respected?

## Networking accuracy checklist

- Verify protocol and port facts against current authoritative documentation.
- Explain when behavior is typical rather than universal.
- Treat provider-specific commands and escalation paths as organization-dependent.
- Never recommend unauthorized access, intrusive scanning, or unapproved changes to production systems.
- Use safe, fictional examples for IP addresses, customers and incidents.
- Include caveats for ICMP filtering, route filtering, VLAN scope, private IPv4 ranges and subnet edge cases.

## Manual test checklist

1. Open `index.html` in a modern browser.
2. Navigate through all top-level views.
3. Complete and refresh a lesson; confirm it remains complete.
4. Answer a quiz correctly and incorrectly; verify feedback and scoring.
5. Flip and mark a flashcard known.
6. Test subnet inputs such as `192.168.10.34/24`, `/26`, `/31` and `/32`.
7. Try an invalid address such as `192.168.10.999`.
8. Open and answer an outage scenario.
9. Filter and expand interview questions.
10. Export progress JSON.
11. Toggle theme and refresh.
12. Check the layout at mobile widths and with reduced motion.

## Pull request guidance

Use a concise title and include the purpose, screenshots when UI changes, manual tests performed, content references, and known limitations. Avoid unrelated formatting changes.