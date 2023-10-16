# Oracle Cloud Day - Kubernetes Demo

## Introduction

This demo shows how to quickly deploy from GitHub Actions to Oracle's Container Engine for Kubernetes (OKE) service.

The GitHub Actions workflow is defined in [`.github/workflows/ci-kubectl.yml`](./.github/workflows/ci-kubectl.yml). On a push, the application in [`apps/http-echo`](./apps/http-echo) is deployed and available at http://129.159.33.175/ (as of Oct 17, 2023).

The container definition for the demo app can be found in [`apps/http-echo/deployment.yml`](./apps/http-echo/deployment.yml). The service definition (which creates the load balancer) can be found in [`apps/http-echo/service.yml`](./apps/http-echo/service.yml).

## Benefits

Your application and CICD process is now defined in code, which gives several benefits:

- That one, tired sysops person can finally go on vacation. This process is defined in code, so the team is able to continue making progress in their absence.

- CICD gives us a process that is automated and can be audited. Any new changes are tracked, must be reviewed, and can be started and completed without any human intervention.

- There is less of a chance of human error. No longer do folks have to remember which SSH/SCP commands to run in order to deploy the application. Also, restores can be automated as well, further reducing risks.
