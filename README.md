# DevOps CI/CD Starter

A beginner-friendly DevOps project demonstrating a small Python Flask application, containerization with Docker, automated testing with pytest, and a CI workflow using GitHub Actions.

## Tools and technologies
- Python and Flask
- Docker
- Git and GitHub
- GitHub Actions
- pytest

## Project workflow
1. A developer pushes code to the `main` branch or opens a pull request.
2. GitHub Actions checks out the code and sets up Python.
3. The workflow installs dependencies and runs automated tests.
4. If the tests pass, Docker builds the application image.

## Run locally
```bash
python -m venv .venv
# Windows:
.venv\Scripts\activate
# macOS/Linux:
source .venv/bin/activate

pip install -r requirements.txt
python app.py
```
Open http://localhost:5000 and http://localhost:5000/health.

## Run tests
```bash
pytest -q
```

## Build and run with Docker
```bash
docker build -t devops-cicd-starter .
docker run -p 5000:5000 devops-cicd-starter
```

## GitHub Actions
The workflow is defined in `.github/workflows/ci-cd.yml`. It runs tests and builds a Docker image on pushes and pull requests targeting `main`.

## Learning outcomes
- Understood a basic CI workflow.
- Automated application tests on code changes.
- Packaged an application using Docker.
- Practiced organizing a repository for collaborative development.

## Note
This is a starter learning project. The workflow builds the Docker image but does not publish it to a container registry or deploy it to a cloud server.
