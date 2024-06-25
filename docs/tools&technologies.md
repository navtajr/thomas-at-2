# Tools and Technologies

## Overview
This document provides an overview of the tools and technologies used in our developer platform. It includes instructions on how to use these tools to develop, deploy, and monitor applications.

## GitHub
GitHub is our chosen platform for version control. All code should be pushed to our GitHub repositories.

- To clone a repository: `git clone <repository_url>`
- To push changes: `git push origin <branch_name>`

## Backstage
Backstage is our self-service portal. It allows developers to manage services, monitor health, and discover APIs.

1. To access Backstage, navigate to our Backstage URL in your web browser.
2. Log in with your company credentials.

## ArgoCD
ArgoCD is our GitOps operator. It ensures that our Kubernetes clusters match the state specified in our Git repositories.

1. To access ArgoCD, navigate to our ArgoCD URL in your web browser.
2. Log in with your company credentials.
3. To deploy an application, create an Application resource in your Git repository.

## Argo Workflows
Argo Workflows is used to trigger post-deployment tasks.

- To create a workflow, define a Workflow resource in your Git repository.
- To trigger a workflow, push changes to the Git repository.

## OpenTelemetry
OpenTelemetry provides observability through tracing, metrics, and logs.

1. To use OpenTelemetry, include the OpenTelemetry SDK in your application code.
2. Configure the SDK to export data to our observability backend.

## OpenFeature
OpenFeature is used for feature flagging.

- To create a feature flag, use the OpenFeature API in your application code.
- To toggle a feature flag, use the OpenFeature dashboard.

## Keptn
Keptn provides deployment observability.

1. To use Keptn, include the Keptn SDK in your application code.
2. Configure the SDK to send deployment events to our Keptn instance.

## KubeAudit
KubeAudit provides additional cluster-level security checks.

- KubeAudit runs automatically on our Kubernetes clusters.
- To view KubeAudit reports, navigate to our KubeAudit dashboard.

## KubeHunter
KubeHunter provides additional security checks.

- KubeHunter runs automatically on our Kubernetes clusters.
- To view KubeHunter reports, navigate to our KubeHunter dashboard.

## Dynatrace
Dynatrace is our observability, security, and automation platform.

1. To use Dynatrace, include the Dynatrace OneAgent in your application code.
2. Configure the OneAgent to send data to our Dynatrace instance.

## Conclusion
This document provides a high-level overview of the tools and technologies used in our developer platform. For more detailed instructions, please refer to the individual documentation for each tool.

