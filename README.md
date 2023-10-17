# Oracle Cloud Day - Kubernetes Demo

## Introduction

This demo shows how to quickly deploy an application from GitHub Actions to Oracle's Container Engine for Kubernetes (OKE) service. On git push, the application defined in [`apps/http-echo`](./apps/http-echo) is deployed by GitHub Actions. The application is deployed to OKE, a load balancer is created, and the application is available at http://129.159.33.175/.

GitHub Actions is a Continuous Integration and Continuous Delivery ([CI/CD](https://en.wikipedia.org/wiki/CI/CD)) service, managed by GitHub. It's a system for automating building, testing, and deploying code.

Oracle Container Engine for Kubernetes ([OKE](https://www.oracle.com/cloud/cloud-native/container-engine-kubernetes/)) is a Kubernetes as a service platform, managed by Oracle. [Kubernetes](https://en.wikipedia.org/wiki/Kubernetes) is an open-source container orchestration system for automating software deployment, auto-scaling, and operations.

## Code

The GitHub Actions workflow is defined in [`.github/workflows/ci-kubectl.yml`](./.github/workflows/ci-kubectl.yml).

The container definition for the demo app can be found in [`apps/http-echo/deployment.yml`](./apps/http-echo/deployment.yml).

The service definition (which creates the load balancer) can be found in [`apps/http-echo/service.yml`](./apps/http-echo/service.yml).

## Benefits

Your application and CICD process is now defined in code, which gives several benefits:

- That one, tired sysops person can finally go on vacation. This process is defined in code, so the team is able to continue making progress in their absence.

- CICD gives us a process that is automated and can be audited. Any new changes are tracked, must be reviewed, and can be started and completed without any human intervention.

- There is less of a chance of human error. No longer do folks have to remember which SSH/SCP commands to run in order to deploy the application. Also, restores can be automated as well, further reducing risks.
