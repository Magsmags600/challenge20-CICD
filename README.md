# Challenge 20 - Fullstack Application CI/CD Workflow

This project implements a CI/CD pipeline for a fullstack web application, designed for streamlined development and deployment workflows. The CI/CD setup uses GitHub Actions to automate testing and deployment, ensuring quality and consistent releases.

## Workflow Overview

1. **Feature Branches and Development**: 
   - Developers create feature branches for new features or bug fixes.
   - All feature branches are merged into the `develop` branch through Pull Requests (PRs).

2. **Cypress Testing on `develop` PRs**:
   - When a Pull Request is created for the `develop` branch, GitHub Actions triggers automated tests.
   - Cypress component tests are executed to verify the integrity of the new code.
   - Only if all tests pass, the PR can be approved and merged into `develop`.

3. **Deployment on `main` Merge**:
   - When code from `develop` is merged into the `main` branch, a GitHub Action automatically deploys the latest code to [Render](https://render.com/).
   - This ensures the main branch deployment is always up to date with the latest tested features.

## Getting Started

To set up this project:

1. **Clone the Repository**: Clone the repository to your local environment.
2. **Set Up GitHub Actions**: Configure two GitHub Actions workflows:
   - **Testing Workflow**: Runs Cypress component tests on any Pull Requests to `develop`.
   - **Deployment Workflow**: Deploys the application to Render upon merging `develop` to `main`.
3. **Set Up Render Deployment**:
   - Deploy the application to Render and configure MongoDB as required.
   - Disable Auto-Deploy in Render settings and use the Render `Deploy hook` URL in GitHub Actions.

## Required Resources

- [Render Deploy Hooks](https://docs.render.com/deploy-hooks): For setting up the deployment trigger from GitHub Actions.
- [GitHub Repo Secrets](https://docs.github.com/en/actions/security-guides/using-secrets-in-github-actions): To store Render API key and deploy hook URL securely for use in GitHub Actions.

## Links
# https://github.com/Magsmags600/challenge20-CICD
# https://challenge20-cicd.onrender.com

## License

This project is licensed under the MIT License.

---

© 2024 All rights reserved.
