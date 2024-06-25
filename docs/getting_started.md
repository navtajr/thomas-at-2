# Getting Started
## Overview
Welcome to the Developer Platform! This platform is designed to streamline your development workflow using the following tools and technologies:

- **GitHub**: Source code repository.
- **Backstage**: Self-service portal.
- **ArgoCD**: GitOps operator.
- **Argo Workflows**: Post-deployment tasks automation.
- **OpenTelemetry**: Standard observability.
- **OpenFeature**: Feature flagging.
- **Keptn**: Deployment observability.
- **KubeAudit**: Cluster-level security checks.
- **KubeHunter**: Additional security checks.
- **Dynatrace**: Observability, security, and automation.

## Accessing Backstage
1. **Login**: Visit the Backstage portal and log in with your company credentials.
2. **Dashboard**: Upon logging in, you'll be taken to the main dashboard where you can find various templates and services.

## Selecting a Template
1. **Navigate to Templates**: Go to the "Templates" section in Backstage.
2. **Choose a Template**: Select a template based on your project needs. Each template is pre-configured with integrations for the tools listed above.

## GitHub: Managing Your Code
- **Creating a Repository:**
    1. In Backstage, use the "Create Repository" template.
    2. Fill in the necessary details such as repository name, description, and visibility.
    3. Click "Create" to set up your repository on GitHub.
- **Cloning a Repository**:<br />
  ```bash
  git clone https://github.com/your-org/your-repo.git
  ```
- **Committing Changes**:<br />
  ```bash
  git add .
  git commit -m "Your commit message"
  git push origin main
  ```

## ArgoCD: Deploying Your Application
1. **Configuration:**
  Use the "ArgoCD Configuration" template in Backstage to generate necessary configuration files.
2. **Deploy**:
    - **Initial Setup**:<br />
  ```bash
  kubectl apply -f argo-cd/install.yaml
  ```
    - **Sync Application**:<br />
  ```bash
  argocd app create my-app --repo https://github.com/your-org/your-repo.git --path ./path-to-your-manifests --dest-server https://kubernetes.default.svc --dest-namespace default
  argocd app sync my-app
  ```

## Argo Workflows: Automating Post-Deployment Tasks
1. **Workflow Templates:**
  Select the "Argo Workflows Template" in Backstage to create workflow definitions.
2. **Triggering Workflows**:
  ```
  argo submit --watch my-workflow.yaml
  ```

## OpenTelemetry: Observability
1. **Instrumenting Your Code:**
  Use the "OpenTelemetry Setup" template to integrate observability into your services.
2. **Viewing Traces**:
    1. Ensure your service is emitting traces.
    2. Use Dynatrace to visualize and analyze trace data.

## OpenFeature: Feature Flagging
1. **Setup:**
  Use the "OpenFeature Integration" template in Backstage to set up feature flags
2. **Usage**:
    ```sh
    if (openFeature.isEnabled("new-feature")){
      // New feature code
    } else {
      // Old feature code
    }
    ```
## KubeAudit and KubeHunter: Security Checks
1. **Setup:**
  Use the "KubeAudit & KubeHunter Configuration" template in Backstage.
2. **Running Security Checks**:
  ```sh
  keptn send event new-artifact --project=myproject --service=myservice --image=myimage --tag=mytag
  ```

## Keptn: Deployment Observability
1. **Setup:**
  Select the "Keptn Integration" template to configure Keptn for your deployments.
2. **Usage**:
    - **KubeAudit**:<br />
    ```bash
    kubeaudit all
    ```
    - **KubeHunter**:<br />
    ```bash
    kube-hunter --remote your-cluster-ip
    ```

## Dynatrace: Observability, Security, and Automation
1. **Setup:**
  Use the "Dynatrace Integration" template to configure monitoring and observability.
2. **Usage**:
  Monitor your services via the Dynatrace dashboard for real-time insights.

## Best Practices
  - **Consistent Naming:**
    Use meaningful and consistent names for repositories, services, and deployments.
  - **Documentation**:
    Keep your code well-documented to facilitate collaboration.
  - **Security:**
    Regularly run security checks using KubeAudit and KubeHunter.
  - **Observability**:
    Ensure all services are instrumented with OpenTelemetry and monitored in Dynatrace.

## Troubleshooting
  - **Common Issues:**
    Refer to the troubleshooting section in each tool's documentation.
  - **Support**:
    KContact the platform engineering team for assistance.
