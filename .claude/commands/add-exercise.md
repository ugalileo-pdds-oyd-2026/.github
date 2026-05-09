Add a solved exercise entry to profile/README.md.

## Usage

/add-exercise <repo-url> [repo-url ...]

## Steps

1. Read `profile/README.md` to find the current state of the "Solved Exercises" section.
2. For each URL provided, derive the repo name from the URL and fetch its README:
   ```bash
   gh api repos/ugalileo-pdds-oyd-2026/<repo-name>/readme --jq '.content' | base64 -d
   ```
3. Write a one-sentence description from the "Teacher's Intent" section (or equivalent). High-level only — what skill is targeted and what the key takeaway is. No CLI commands, no file names, no step-by-step details.
4. Determine the session and exercise numbers from the repo name (e.g., `exercise-1-2` → Exercise 1.2, Session 1) and confirm the session topic in `syllabus.md`.
5. Add or extend the correct `### Session N — <Topic>` subsection under "Solved Exercises" in `profile/README.md`. Append new sessions at the bottom; append new items within a session in the order provided.

## Format

Each bullet must follow this pattern exactly:
```
* **[Exercise N.M: <Title>](<url>):** <one-sentence description>
```

Do not modify any other section of `profile/README.md`.
