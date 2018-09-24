# GitHub Exporter for Prometheus

Exposes metrics for target repository from the GitHub API, to a Prometheus compatible endpoint.

## Configuration

This exporter is setup to take input from environment variables:

### Required
* `GITHUB_TOKEN` If supplied, enables the user to supply a github personal access token that allows the API to be queried more often. Optional, but recommended.
* `REPO` The repos you wish to monitor, expected in the format "owner/repo"

## How to run

### Docker compose
```
docker-compose up --build
```

### Locally
Supply the personal access token and the target repo you want to monitor.
```
GITHUB_TOKEN=your_github_token REPO=owner/repo npm start
```

## Metrics

Metrics will be made available on port 5001 by default
An example of these metrics can be found in the `METRICS.md` markdown file in the root of this repository
