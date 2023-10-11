# Oracle Cloud Day - Kubernetes Demo

This demo shows how to quickly deploy from GitHub Actions to Oracle's Container Engine for Kubernetes (OKE) service.

On a push, the application in `apps/http-https-echo` is deployed and available at http://192.9.136.65/ (as of Oct 17, 2023).

The container definition can be found in [`apps/http-https-echo/deployment.yml`](./apps/http-https-echo/deployment.yml). The service definition can be found in [`apps/http-https-echo/service.yml`](./apps/http-https-echo/service.yml).
