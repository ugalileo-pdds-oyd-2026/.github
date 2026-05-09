# Claude Instructions — OyD 2026 GitHub Profile

## Adding Solved Exercises to the README

When the instructor asks to add a solved exercise to `profile/README.md`, follow these steps:

1. **Read the current README** at `profile/README.md` to find the existing "Solved Exercises" table and understand the current state.

2. **Fetch the exercise repo's README** using the GitHub CLI to understand what the exercise is about:
   ```bash
   gh api repos/ugalileo-pdds-oyd-2026/<repo-name>/readme --jq '.content' | base64 -d
   ```

3. **Write a one-paragraph description** based on the repo's "Teacher's Intent" section (or equivalent). The description should explain:
   - What concept or skill the exercise targets
   - What students do (the tasks)
   - What they learn (the takeaway)
   Keep it to 2–3 sentences — concise enough to fit a table cell.

4. **Add a new row** to the Solved Exercises table in `profile/README.md`, following the existing format:
   ```
   | <number> | [<Title>](<url>) | <session> | <description> |
   ```
   - Exercise numbers follow the pattern `<session>.<exercise-within-session>` (e.g., `1.1`, `1.2`, `2.1`).
   - Session number matches the course schedule in `syllabus.md`.
   - Append new rows at the bottom of the table.

5. **Do not change any other section** of the README unless explicitly asked.

## Course Context

- **Organization:** `ugalileo-pdds-oyd-2026`
- **Exercise repos** follow the naming convention `exercise-<session>-<number>` (e.g., `exercise-1-1`, `exercise-2-1`).
- The course schedule and session topics are in `syllabus.md`. Use it to confirm which session an exercise belongs to.
