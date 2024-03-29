# GitOps
| Author | Created On | Last Updated | Document Version | Last Updated By |
| ------ | ---------- | ------------ | ---------------- | --------------- |
| Vishal Kumar Kesarwani | 12-01-2024 | 16-01-2024   | v1 | Vishal |
***
# Table of Contents

+ [Introduction](#Introduction)
+ [Why GitOps](#Why-GitOps)
+ [GitOps Principles ](#GitOps-Principles )
+ [GitOps Tools ](#GitOps-Tools )
+ [GitOps Workflows ](#GitOps-Workflows )
+ [Benefits of GitOps](#Benefits-of-GitOps)
+ [Drawbacks of GitOps](#Drawbacks-of-GitOps)
+ [Contact Information](#Contact-Information)
+ [References](#References)

***
# Introduction
<img width="260" length="100" alt="GitOps" src="https://github.com/avengers-p7/Documentation/assets/156056413/6d918855-2887-4fe4-b731-a66c683f3388">
 
GitOps is code-based infrastructure and operational procedures that rely on Git as a source control system. It’s an evolution of Infrastructure as Code (IaC) and a DevOps best practices that leverages Git as the single source of truth, and control mechanism for creating, updating, and deleting system architecture.
***
# Why GitOps

GitOps is a modern approach to managing and deploying infrastructure and applications that leverages Git as the central source of truth. Here are key points **:**
| Feature | Description |
| --- | --- |
| **Version Control** | GitOps uses Git for version control, enabling teams to track changes, collaborate effectively, and maintain an audit trail of modifications. |
| **Declarative Configuration** | GitOps relies on declarative configurations, specifying the desired state rather than procedural steps. This enhances readability and reduces configuration drift. |
| **Infrastructure as Code (IaC)** | GitOps promotes Infrastructure as Code (IaC) principles, allowing for automated provisioning and management of infrastructure. |
| **Automation** | Automation is a core aspect of GitOps, facilitating continuous delivery and deployment, reducing human errors, and ensuring consistent and repeatable processes. |
| **Consistency Across Environments** | GitOps ensures consistency in configurations and infrastructure across different environments, from development to production. |
| **Rollback and Rollforward** | GitOps simplifies the process of rolling back to previous states or applying changes in a controlled manner by leveraging Git's versioning capabilities. |
| **Collaboration and Visibility** | GitOps encourages collaboration among team members through Git's collaboration features, promoting better communication and visibility into system changes. |
| **Multi-Cloud and Hybrid Cloud** | GitOps is adaptable to multi-cloud and hybrid cloud environments, making it suitable for organizations with diverse infrastructure needs. |
***
# GitOps Principles 
| Feature | Description |
| --- | --- |
| **Declarative** | System configurations are expressed declaratively, leveraging Git as the authoritative source of truth. This approach simplifies deployment, rollback, and disaster recovery by focusing on defining the desired state rather than explicit instructions. |
| **Versioned and Immutable** | The system's canonical state is stored and versioned in Git, offering a reliable repository for configurations. This enables straightforward rollbacks and creates an immutable version store, essential for maintaining a secure audit trail. |
| **Pulled Automatically** | Approved changes are automatically applied to the system, promoting an automated deployment workflow. GitOps allows for separation between the defined state and execution, minimizing manual interventions and emphasizing automated tests and checks.| 
| **Continuously Reconciled** | Software agents continuously monitor and alert on disparities between the declared and actual system states. These agents contribute to self-healing capabilities, addressing discrepancies and errors in real-time. |
***
# GitOps Tools 
| **Name** | **Description** |
| -------- | --------------- |
| **ArgoCD** | Declarative continuous deployment for Kubernetes |
| **Flux** | Open and extensible continuous delivery solution for Kubernetes. Powered by GitOps Toolkit |
| **Jenkins X** | a CI/CD platform for Kubernetes that provides pipeline automation, built-in GitOps and preview environments. |
| **BuildPiper** | BuildPiper is IDP capable of CI/CD , GitOps , JiraOps , etc.  
| **Autoapply** | Automatically apply changes from a Git repository to a Kubernetes cluster |
| **Helm Operator** | Automates Helm Chart releases in a GitOps manner |
| **Flagger** | Progressive delivery Kubernetes operator (Canary, A/B testing and Blue/Green deployments automation) |
| **KubeStack** | GitOps framework using Terraform for Cloud Kubernetes distros (AKS, GKE, and EKS) with CI/CD examples for common tools. |
| **Weave GitOps** | Weave GitOps is a simple open source developer platform for people who want cloud native applications, without needing Kubernetes expertise. |
| **Werf** | GitOps tool with advanced features to build images and deploy them to Kubernetes (integrates with any existing CI system) |
| **PipeCD** | Continuous Delivery for Declarative Kubernetes, Serverless and Infrastructure Applications |
| **Gimlet** | The Flux-based Internal Developer Platform |
***
# GitOps Workflows 
<img width="600" length="300" alt="GitOps" src="https://github.com/avengers-p7/Documentation/assets/156056413/e715aa24-9f48-465c-bfca-7a34a27e4a6f"> 

*** 
# Benefits of GitOps
The underlying Git protocol isn't resource-intensive and is open source. It offers the following additional benefits:

* Increased productivity through the enablement of CD and deployment.
* Reliability through declarative states, versioned storage, continuous state reconciliation, revert and rollback, and fork features.
* A reduced number of potential variables in infrastructure management
* Visibility and a clear change history.
*** 
# Drawbacks of GitOps
Some disadvantages of GitOps, however, include these drawbacks:

* GitOps requires training for teams unfamiliar with Git and version control.
* GitOps is more suited for stateless applications, posing challenges for stateful workloads.
* GitOps doesn't offer a way to manage authentication or other sensitive data without additional tooling.

***
## Contact Information:
| Name | Email address |
| ---- | ------------- |
| vishal | vishal.kesarwani.snaatak@mygurukulam.co |
***
## References:
| Source | Description |
| ------ | ----------- |
| https://www.techtarget.com/searchitoperations/definition/GitOps  | Gitops Features |
| https://www.site24x7.com/learn/what-is-gitops.html | Gitops Features |
| https://dev.to/arafetki/gitops-infra-as-code-done-right-2ojg | Gitops Workflow |
| https://www.weave.works/technologies/gitops/  | Gitops Principles |

