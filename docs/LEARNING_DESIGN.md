# TutorX Learning and Assessment Design

## Learning loop

Each study session should follow a simple loop:

1. **Learn:** read one short lesson with definitions and an example.
2. **Retrieve:** answer a flashcard before revealing the answer.
3. **Apply:** solve a quiz or scenario using the concept.
4. **Explain:** teach the idea back in the learner's own words.
5. **Review:** revisit missed or difficult concepts in a later session.

## Why the experience is structured this way

- Active recall makes the learner retrieve information rather than passively reread it.
- Spaced review should gradually increase the interval for cards the learner knows and shorten it for cards they miss.
- Immediate feedback explains the reasoning behind an answer.
- Scenario practice transfers vocabulary into operational judgment.
- Low-stakes quizzes encourage repeated practice and reveal gaps before a mock interview.

## Question-writing standards

1. Ask one clear thing per question.
2. Use plausible distractors based on common misconceptions.
3. Keep only one best answer unless the prompt explicitly says select multiple.
4. Explain why the correct answer is correct and why the misconception is risky.
5. Avoid trick questions, vague absolutes, and ambiguous wording.
6. Tag each item with section, lesson, difficulty, and learning objective as the bank grows.
7. Review calculations and edge cases before publishing.

## Scoring

XP is intended to encourage practice, not rank learners or imply certification. The current prototype awards XP for lesson completion, flashcard recall, quizzes, and successful scenarios. Repeated actions may award additional XP; future versions should define anti-farming rules and mastery thresholds.

Suggested mastery guidance:

- 90–100%: ready to move forward, but keep reviewing.
- 80–89%: good working understanding; revisit missed explanations.
- 60–79%: practise the relevant lesson and retake the quiz.
- Below 60%: re-read the lesson, use flashcards, and retest without time pressure.

## Flashcard lifecycle

Front: one definition, distinction, sequence or scenario prompt. Back: concise answer plus a caveat where needed. The learner should mark a card as known only after attempting recall.

Recommended future improvement: implement a simple spaced repetition schedule using `dueAt`, `intervalDays`, and `ease` or a simpler box-based Leitner system. Store dates in ISO format and ensure the schedule is robust when the learner's local date changes.

## Scenario scoring rubric

Evaluate the learner's reasoning on:

- Impact and scope assessment.
- Evidence collection and correlation.
- Safe, authorized troubleshooting.
- Correct fault-boundary reasoning.
- Ticket quality and timestamped documentation.
- Customer communication and SLA-aware escalation.
- Verification before declaring restoration.

Do not reward reckless production changes, unsupported diagnoses, or invented restoration estimates.

## Interview preparation rubric

Score each response from 0 to 2 across five dimensions:

- Technical accuracy.
- Clear explanation.
- Practical example.
- Structured troubleshooting or reasoning.
- Integrity, safety and escalation awareness.

Total: 10 points. A strong answer should be accurate, understandable and operationally safe, not simply long.

## Suggested study schedule

| Week | Focus |
|---|---|
| 1 | Sections 1–2: fundamentals, OSI and TCP/IP. |
| 2 | Section 3: IPv4 addressing and subnetting practice. |
| 3 | Sections 4–5: switching, routing, protocols and ports. |
| 4 | Section 6: telecommunications and optical concepts. |
| 5 | Sections 7–8: troubleshooting and incident management. |
| 6 | Sections 9–10: vendor CLI concepts and NOC operations. |
| 7 | Section 11: mock interviews and mixed review. |

The pace is flexible. Repeat a week when a concept is not yet explainable without prompts.