Create a GitHub repository for a new exercise in the ugalileo-pdds-oyd-2026 organization.

## Usage

/create-exercise-repo <path-to-exercise-markdown>

## Steps

1. Read the markdown file at the given path.

2. Extract from the markdown:
   - **Session number** and **exercise number** — from the heading (e.g., `Exercise 1.1` → session `1`, number `1`).
   - **Title** — the short title after the dash in the heading (e.g., `# Exercise 1.1 — What Will Terraform Do?` → `What Will Terraform Do?`). Strip any markdown bold markers (`**`).

3. Derive the standardized repo name and description:
   - **Repo name:** `exercise-<session>-<number>` (e.g., `exercise-1-1`)
   - **Description:** `Solution to Exercise <session>.<number> of Optimizations and Performance — <Title>` (e.g., `Solution to Exercise 1.1 of Optimizations and Performance — What Will Terraform Do?`)

4. Create the repository in the organization with no README:
   ```bash
   gh repo create ugalileo-pdds-oyd-2026/<repo-name> \
     --public \
     --description "<description>"
   ```

5. Output the resulting repository URL so it can be passed to the next agent.

## Rules

- Do not create any files or push any content to the repository. The repo is intentionally empty — another agent handles that.
- Do not add a README, LICENSE, or .gitignore via `gh repo create` flags.
- The org is always `ugalileo-pdds-oyd-2026`. Never create the repo under a personal account.
- If the repo already exists, stop immediately. Do not attempt to create it under a different name or any variation. Report that you will not proceed and return the existing URL.
