# Claude Instructions — OyD 2026 GitHub Profile

## Skills

Use the repo skills to update `profile/README.md`:

- `/add-demo <url> [url ...]` — fetches each demo repo's README and adds an entry under "Class Demos".
- `/add-exercise <url> [url ...]` — fetches each exercise repo's README and adds an entry under "Solved Exercises".

Both skills handle multiple URLs in one invocation, derive the session from the repo name, confirm the topic from `syllabus.md`, and write a high-level one-sentence description. Do not modify other sections of `profile/README.md` unless explicitly asked.

## Format reference

Both sections use the same structure:
- `##` heading for the category.
- `###` subsection per session: `Session N — <Topic>` (topic from `syllabus.md`).
- Bulleted list of entries within each session.

Demos: `* **[<Title>](<url>):** <description>`
Exercises: `* **[Exercise N.M: <Title>](<url>):** <description>`

## Course reference

- **Organization:** `ugalileo-pdds-oyd-2026`
- **Demo repos:** `session-<N>-demo-<M>-<slug>`
- **Exercise repos:** `exercise-<session>-<number>`
- **Session topics and dates:** `syllabus.md`
