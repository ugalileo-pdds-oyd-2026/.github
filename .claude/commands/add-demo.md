Add a class demo entry to profile/README.md.

## Usage

/add-demo <repo-url> [repo-url ...]

## Steps

1. Read `profile/README.md` to find the current state of the "Class Demos" section.
2. For each URL provided, derive the repo name from the URL and fetch its README:
   ```bash
   gh api repos/ugalileo-pdds-oyd-2026/<repo-name>/readme --jq '.content' | base64 -d
   ```
3. Write a one-sentence description from the "What students learn" section (or equivalent). High-level only — no CLI commands, no file names, no step-by-step details.
4. Determine the session number from the repo name (e.g., `session-3-demo-2-lambda` → Session 3) and confirm the session topic in `syllabus.md`.
5. Add or extend the correct `### Session N — <Topic>` subsection under "Class Demos" in `profile/README.md`. Append new sessions at the bottom; append new items within a session in the order provided.

## Format

Each bullet must follow this pattern exactly:
```
* **[<Title>](<url>):** <one-sentence description>
```

Do not modify any other section of `profile/README.md`.
