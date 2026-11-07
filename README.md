# Python Continuous Deployment Simulator

## 1. Project Overview

This project demonstrates the basic concepts of Continuous Deployment (CD) using Python. It simulates application deployment across different environments and demonstrates deployment strategies, health checks, approval processes, and rollback operations.

## 2. Project Objectives

- Understand Continuous Deployment concepts.
- Simulate deployment across multiple environments.
- Implement different deployment strategies.
- Demonstrate deployment failure handling.
- Understand rollback mechanisms.
- Use Git and GitHub for version control.

## 3. Technologies Used

- **Programming Language:** Python
- **Code Editor:** Visual Studio Code
- **Version Control:** Git
- **Repository Hosting:** GitHub

## 4. Deployment Environments

The simulator supports four environments:

- Development (DEV)
- Testing
- Staging
- Production (PROD)

## 5. Deployment Strategies

### Direct Deployment
Deploys a new application version directly to the selected environment.

### Blue-Green Deployment
Simulates two environments (Blue and Green). The new version is tested before switching traffic to it.

### Canary Deployment
Gradually increases traffic to the new version through 10%, 25%, 50%, and 100% stages.

## 6. Features

- Deployment status monitoring.
- Production deployment approval.
- Automatic approval simulation.
- Health check simulation.
- Deployment failure simulation.
- Rollback to the previous version.
- JSON-based deployment state management.

## 7. How to Run

Make sure Python is installed.

Clone the repository:

```bash
git clone https://github.com/meghanaun25-cpu/CD-Deployment.git
```

Navigate into the project:

```bash
cd CD-Deployment
```

Check deployment status:

```bash
python deploy.py status
```

Run a direct deployment:

```bash
python deploy.py deploy --env dev --version v1.1 --strategy direct
```

Run a Blue-Green deployment:

```bash
python deploy.py deploy --env prod --version v2.0 --strategy blue-green
```

Run a Canary deployment:

```bash
python deploy.py deploy --env prod --version v3.0 --strategy canary
```

Perform rollback:

```bash
python deploy.py rollback --env prod
```

## 8. Failure Testing

The simulator supports the `--fail-health` option to demonstrate failed health checks.

Example:

```bash
python deploy.py deploy --env prod --version v2.1 --strategy blue-green --fail-health
```

## 9. Project Files

- `deploy.py` – Main Python deployment simulator.
- `deployment_state.json` – Stores deployment state and version information.
- `README.md` – Project documentation.

## 10. Conclusion

This project provides a practical understanding of Continuous Deployment concepts through a Python-based simulation. It demonstrates deployment strategies, environment management, health checks, failure handling, and rollback operations.

**Note:** This is an educational simulator. It does not deploy applications to actual production servers or manage real user traffic.
