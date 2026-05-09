Create a GitHub repository for a new class demo in the ugalileo-pdds-oyd-2026 organization.

## Usage

/create-demo-repo <path-to-teacher-guide-markdown>

## Steps

1. Read the markdown file at the given path.

2. Extract from the markdown:
   - **Session number** — from the session line near the top (e.g., `Session 3 · Compute Automation + EKS Provisioning` → `3`).
   - **Demo number** — from the heading (e.g., `# Demo 1 — EC2 Module + Security Group` → `1`).
   - **Title** — the short label after the dash in the heading (e.g., `EC2 Module + Security Group`).

3. Derive the standardized repo name and description:
   - **Slug:** a short, lowercase, hyphenated identifier derived from the title. Keep it concise — prefer the core technology name(s) over the full title (e.g., `EC2 Module + Security Group` → `ec2`, `Kubernetes Basics with FastAPI` → `k8s-fastapi`, `Lambda + API Gateway` → `lambda`).
   - **Repo name:** `session-<N>-demo-<M>-<slug>` (e.g., `session-3-demo-1-ec2`)
   - **Topic label:** a short, human-readable label for the description, slightly more descriptive than the slug (e.g., `Compute: EC2`, `Kubernetes Basics`, `Terraform Core Mechanics`).
   - **Description:** `Optimizations and Performance - Session <N> - Demo <M> - <Topic label>` (e.g., `Optimizations and Performance - Session 3 - Demo 1 - Compute: EC2`)

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
