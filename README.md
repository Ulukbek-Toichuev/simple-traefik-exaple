# Task 1.9: Getting Started with Docker Compose

In this task, you will set up a fully operational application using Docker Compose, one of the simplest methods for configuring an application in a local development environment. It is also occasionally used to deploy applications in production.

## Study Topics

- Docker Compose syntax (docker-compose)
- Networking in Docker Compose
- Traefik setup and usage
- Persistent storage in Docker Compose

## Task

Create a docker-compose file for the Firefly III application. The file should include the following services: firefly-iii, firefly-iii-data-importer, postgresql, cron, and a redis cache. Additionally, add traefik as a reverse proxy to route traffic to both firefly-iii and firefly-iii-data-importer. Since this setup is local, differentiate the services either by port or by hostname (hostnames can be added to /etc/hosts).

- Create a docker-compose file that includes all the listed services.
- Add volumes for the database and any other necessary components, as specified in the Firefly III Compose file (refer to the official Firefly III Compose documentation).
- Configure Traefik as a reverse proxy to provide access to the front ends of firefly-iii and firefly-iii-data-importer.
- Include a self-signed OpenSSL certificate in the Traefik configuration.
- Set up an HTTP-to-HTTPS redirect in Traefik for both firefly-iii and firefly-iii-data-importer.

## Notes

- Port 8080 on the host will map to port 80 in the VM.
- Port 8443 on the host will map to port 443 in the VM.
- Use the existing Firefly III Compose file and documentation only as references.
- Push the source code to your Foxminded GitLab repository.

## Acceptance Criteria

- The application must be running on the VM and accessible at localhost:8080 from the host via the Traefik reverse proxy.
- Obtain mentor approval for your pull request.

## Submission

Submit the task to the Foxminded GitLab repository as a pull request from a feature branch to the dev branch, using a naming convention like feat/new-shiny-feature.
