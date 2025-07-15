[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=19935519&assignment_repo_type=AssignmentRepo)
# Deployment and DevOps for MERN Applications

## 🚀 Deployment Process

This project uses **GitHub Actions** for Continuous Integration (CI) and Continuous Deployment (CD) of both the frontend (React) and backend (Express.js) applications.

### 1. Continuous Integration (CI)

- Frontend (`frontend-ci.yml`):
  - Runs on every push or pull request affecting the `frontend/` directory.
  - Installs dependencies, runs tests, and builds the React app.
- Backend (`backend-ci.yml`):
  - Runs on every push or pull request affecting the `backend/` directory.
  - Installs dependencies and runs backend tests.

### 2. Continuous Deployment (CD)

- Frontend (`frontend-cd.yml`):
  - Triggers on every push to the `main` branch that affects the `frontend/` directory.
  - Installs dependencies, builds the React app, and deploys it to the configured platform (e.g., Vercel, Netlify, or your custom server).
- Backend (`backend-cd.yml`):
  - Triggers on every push to the `main` branch that affects the `backend/` directory.
  - Installs dependencies, builds the backend (if needed), and deploys it to the configured platform (e.g., Heroku, Render, or your custom server).

### 3. Secrets & Configuration

- Deployment workflows require secrets (API keys, tokens, etc.) to be set in your repository’s **Settings > Secrets and variables > Actions**.
- Example secrets:
  - For Vercel: `VERCEL_TOKEN`, `VERCEL_ORG_ID`, `VERCEL_PROJECT_ID`
  - For Heroku: `HEROKU_API_KEY`, `HEROKU_APP_NAME`, `HEROKU_EMAIL`

### 4. Customizing Deployment

- Update the deployment steps in the workflow files to match your hosting provider.
- Make sure to add any required build or environment configuration.

---
## screenshot of ci/cd in action
<img width="940" height="961" alt="Screenshot from 2025-07-15 21-46-15" src="https://github.com/user-attachments/assets/98ec9fb7-dfe1-476f-9444-c8a445d26230" />
<img width="940" height="961" alt="Screenshot from 2025-07-15 21-39-17" src="https://github.com/user-attachments/assets/a4e0fe2b-a1c3-4e98-bec9-cabbe62208bb" />

URL for the deployed application: https://blog-jx3v.vercel.app/
