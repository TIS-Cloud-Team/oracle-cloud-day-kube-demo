# Oracle Cloud Day - Kubernetes Demo

This demo shows how to quickly deploy from GitHub Actions to Oracle's Container Engine for Kubernetes (OKE) service.

The GitHub Actions workflow is defined in [`.github/workflows/ci-kubectl.yml`](./.github/workflows/ci-kubectl.yml). On a push, the application in `apps/http-echo` is deployed and available at http://152.67.226.107/ (as of Oct 17, 2023).

The container definition for the demo app can be found in [`apps/http-echo/deployment.yml`](./apps/http-echo/deployment.yml). The service definition (which creates the load balancer) can be found in [`apps/http-echo/service.yml`](./apps/http-echo/service.yml).
