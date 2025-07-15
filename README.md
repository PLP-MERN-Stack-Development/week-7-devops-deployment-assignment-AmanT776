[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=19935519&assignment_repo_type=AssignmentRepo)
# Deployment and DevOps for MERN Applications

This assignment focuses on deploying a full MERN stack application to production, implementing CI/CD pipelines, and setting up monitoring for your application.

## Assignment Overview

You will:
1. Prepare your MERN application for production deployment
2. Deploy the backend to a cloud platform
3. Deploy the frontend to a static hosting service
4. Set up CI/CD pipelines with GitHub Actions
5. Implement monitoring and maintenance strategies

## Getting Started

1. Accept the GitHub Classroom assignment invitation
2. Clone your personal repository that was created by GitHub Classroom
3. Follow the setup instructions in the `Week7-Assignment.md` file
4. Use the provided templates and configuration files as a starting point

## Files Included

- `Week7-Assignment.md`: Detailed assignment instructions
- `.github/workflows/`: GitHub Actions workflow templates
- `deployment/`: Deployment configuration files and scripts
- `.env.example`: Example environment variable templates
- `monitoring/`: Monitoring configuration examples

## Requirements

- A completed MERN stack application from previous weeks
- Accounts on the following services:
  - GitHub
  - MongoDB Atlas
  - Render, Railway, or Heroku (for backend)
  - Vercel, Netlify, or GitHub Pages (for frontend)
- Basic understanding of CI/CD concepts

## Deployment Platforms

### Backend Deployment Options
- **Render**: Easy to use, free tier available
- **Railway**: Developer-friendly, generous free tier
- **Heroku**: Well-established, extensive documentation

### Frontend Deployment Options
- **Vercel**: Optimized for React apps, easy integration
- **Netlify**: Great for static sites, good CI/CD
- **GitHub Pages**: Free, integrated with GitHub

## CI/CD Pipeline

The assignment includes templates for setting up GitHub Actions workflows:
- `frontend-ci.yml`: Tests and builds the React application
- `backend-ci.yml`: Tests the Express.js backend
- `frontend-cd.yml`: Deploys the frontend to your chosen platform
- `backend-cd.yml`: Deploys the backend to your chosen platform

## Submission

Your work will be automatically submitted when you push to your GitHub Classroom repository. Make sure to:

1. Complete all deployment tasks
2. Set up CI/CD pipelines with GitHub Actions
3. Deploy both frontend and backend to production
4. Document your deployment process in the README.md
5. Include screenshots of your CI/CD pipeline in action
6. Add URLs to your deployed applications

## Resources

- [GitHub Actions Documentation](https://docs.github.com/en/actions)
- [MongoDB Atlas Documentation](https://docs.atlas.mongodb.com/)
- [Render Documentation](https://render.com/docs)
- [Railway Documentation](https://docs.railway.app/)
- [Vercel Documentation](https://vercel.com/docs)
- [Netlify Documentation](https://docs.netlify.com/) 
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

URL for the deployed application: https://blog-jx3v.vercel.app/