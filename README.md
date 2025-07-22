# 🚀 GitHub Actions Workflow Project

> ⚙️ A project showcasing CI/CD automation using GitHub Actions with workflows for deployment, testing, and GitHub issue event handling.

---

## 📄 Workflows

### 1. Deployment 1
- **Trigger**: On every `push`
- **Purpose**: Runs a linear CI/CD pipeline.
- **Steps**:
  - Checkout code
  - Install dependencies
  - Lint the code
  - Run tests
  - Build the project
  - Deploy (currently just a placeholder)

### 2. Deployment 2
- **Trigger**: On every `push`
- **Purpose**: Runs the same steps as above, but in separate dependent jobs:
  - `lint` → `test` → `deploy`
- Each job only runs if the previous one succeeds.

### 3. Handle Issues
- **Trigger**: On GitHub `issues` events (open, edit, close)
- **Purpose**: Outputs the GitHub issue event details for logging or future automation.

---

## 🛠️ Requirements

Ensure your Node.js project includes the following scripts in `package.json`:

```json
"scripts": {
  "lint": "eslint .",
  "test": "vitest",
  "build": "your-build-comman

