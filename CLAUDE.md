# Claude Instructions — OyD 2026 GitHub Profile

## Format rules for profile/README.md

Both "Class Demos" and "Solved Exercises" sections use the same structure:

- An `##` section heading for the category ("Class Demos", "Solved Exercises").
- An `###` subsection for each session, titled `Session N — <Topic>`. Get the topic from `syllabus.md`.
- Inside each session, a bulleted list. Each bullet follows this pattern:
  ```
  * **[<Title>](<url>):** <one-sentence description — high-level only, no commands>
  ```
- Descriptions must be high-level: what concept it covers and what students learn. No CLI commands, no file names, no step-by-step details.
- Append new sessions at the bottom of each section. Append new items within a session in the order they were added.

## Adding a Class Demo

When the instructor provides a demo repo URL:

1. Read `profile/README.md` to find the current state of the "Class Demos" section.
2. Fetch the demo repo's README:
   ```bash
   gh api repos/ugalileo-pdds-oyd-2026/<repo-name>/readme --jq '.content' | base64 -d
   ```
3. Write a one-sentence description from the "What students learn" section (or equivalent). Focus on the concept, not the steps.
4. Determine the session number from the repo name (e.g., `session-3-demo-2-lambda` → Session 3) and confirm the session topic in `syllabus.md`.
5. Add or extend the correct `### Session N` subsection in the "Class Demos" section of `profile/README.md`.

Demo repo naming convention: `session-<N>-demo-<M>-<slug>` (e.g., `session-2-demo-1-k8s-fastapi`).

## Adding a Solved Exercise

When the instructor provides an exercise repo URL:

1. Read `profile/README.md` to find the current state of the "Solved Exercises" section.
2. Fetch the exercise repo's README:
   ```bash
   gh api repos/ugalileo-pdds-oyd-2026/<repo-name>/readme --jq '.content' | base64 -d
   ```
3. Write a one-sentence description from the "Teacher's Intent" section (or equivalent). Focus on the skill targeted and the key takeaway.
4. Determine the session and exercise numbers from the repo name (e.g., `exercise-1-2` → Exercise 1.2, Session 1) and confirm the session topic in `syllabus.md`.
5. Add or extend the correct `### Session N` subsection in the "Solved Exercises" section of `profile/README.md`.

Exercise repo naming convention: `exercise-<session>-<number>` (e.g., `exercise-1-2`).
Exercise label format: `Exercise <session>.<number>` (e.g., `Exercise 1.2`).

## Course reference

- **Organization:** `ugalileo-pdds-oyd-2026`
- **Session topics and dates:** `syllabus.md`
- **Do not modify** any other section of `profile/README.md` unless explicitly asked.
