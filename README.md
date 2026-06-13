# CI/CD Pipeline with Automated Testing & Containerisation

![CI](https://github.com/Ayeshaa-w/ci-cd-python/actions/workflows/ci.yml/badge.svg)

## What this project is
A production-style CI/CD pipeline built around a Flask REST API.
The focus is the engineering system, not the app itself.

## The Pipeline
Every push to main triggers automatically:
1. GitHub Actions spins up Ubuntu runner
2. Pytest runs all 6 tests
3. If any test fails — pipeline stops. Docker never builds.
4. If all pass — Docker image is built.

## API Endpoints
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | /items | Create item |
| GET | /items | Get all items |
| GET | /items/:id | Get one item |
| DELETE | /items/:id | Delete item |

## Run locally
docker build -t flask-api .
docker run -p 5000:5000 flask-api

## Tech Stack
Python, Flask, Pytest, Docker, GitHub Actions, Kubernetes
