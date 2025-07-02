---
title: "Week #4"
---

# **Week #4**

## Testing and QA

- We implemented automated API tests for the backend using pytest and FastAPI’s TestClient.
- The tests cover all main endpoints: root, metals list, historical data, and forecast endpoints.
- Linting is enforced with flake8 to ensure code quality and style consistency.
- Manual QA was performed for the frontend by opening the site in a browser and verifying all UI features and interactions.

### Evidence of test execution

- [Tests with linting screenshot](https://raw.githubusercontent.com/IU-Capstone-Project-2025/Metalytics/refs/heads/main/Assets/backend-test.png) or [link to job](https://github.com/IU-Capstone-Project-2025/Metalytics/actions/runs/16028126489/job/45221300532).
- [Docker test screenshot](https://raw.githubusercontent.com/IU-Capstone-Project-2025/Metalytics/refs/heads/main/Assets/docker-test.png) or [direct link](https://github.com/IU-Capstone-Project-2025/Metalytics/actions/runs/16028126489/job/45221300559).
- [Frontend UI screenshot](https://raw.githubusercontent.com/IU-Capstone-Project-2025/Metalytics/refs/heads/main/Assets/front-test.png).

## CI/CD

- We used GitHub Actions for continuous integration.
- The workflow installs dependencies, runs linting (flake8), runs backend tests (pytest), and builds the backend Docker image.
- The workflow also runs the backend Docker container and checks the /health endpoint to ensure the app starts correctly.

Challenges faced:
- We encountered a ModuleNotFoundError for main in tests, which was fixed by setting PYTHONPATH=. in the workflow.
- Docker health checks required a sleep to allow the container to start before testing the endpoint.

### Links to CI/CD configuration files

- [Backend CI workflow](https://github.com/IU-Capstone-Project-2025/Metalytics/blob/main/.github/workflows/ci.yml).
- [Backend Dockerfile](https://github.com/IU-Capstone-Project-2025/Metalytics/blob/main/backend/Dockerfile).
- [Frontend Dockerfile](https://github.com/IU-Capstone-Project-2025/Metalytics/blob/main/frontend/Dockerfile).

## Deployment

### Staging

*Details about the deployment process, environment setup for staging environment*

### Production

*If you focus on bonus points, describe the production deployment process, environment setup for production environment, public domain name and VDS setup*
*ATTENTION: You can put this section in ANY future report (weeks 4,5,6)*

## Vibe Check

*Facilitate a team health check. Discuss progress, roadblocks, and team dynamics. Ensure everyone feels heard.*

# Weekly commitments

## Individual contribution of each participant

*...*

## Plan for Next Week

*...*

## Confirmation of the code's operability

We confirm that the code in the main branch:
- [ ] In working condition.
- [ ] Run via docker-compose (or another alternative described in the `README.md`).
