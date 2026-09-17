ArgoCD Developer UI Walkthrough — OnePass Platform

1. ArgoCD UI Overview

After logging in, the Applications page provides an overview of all applications managed by ArgoCD.

Screenshot: Application Dashboard

The dashboard provides visibility into:

* Application name
* Deployment status
* Health status
* Sync status
* Repository information
* Target environment

Health Status

* Healthy → Application resources are running correctly.
* Progressing → Deployment changes are being applied, or application resources are still starting.
* Degraded → One or more application resources are unhealthy or experiencing issues.

Sync Status

* Synced → The Kubernetes environment matches the configuration stored in Git.
* OutOfSync → The Kubernetes environment differs from the configuration stored in Git and requires synchronization.

⸻

2. Understanding an Application

Selecting an application opens the application details page, which provides a detailed view of the Kubernetes resources managed by ArgoCD.

Screenshot: Application Detail / Resource Tree

The resource tree helps developers understand the components deployed as part of their application, including:

* Deployments
* Pods
* Services
* ConfigMaps
* Other Kubernetes resources

This view can be used to verify whether application components are running correctly and identify any unhealthy resources.

⸻

3. Reviewing Application Changes

The Diff view allows developers to compare the current Kubernetes state with the desired state stored in Git.

Screenshot: Diff View

The Diff view helps review:

* Container image changes
* Configuration updates
* Environment variable changes
* Replica count changes
* Kubernetes manifest updates

Before syncing an application, reviewing the Diff helps confirm that the expected changes will be applied.

⸻

4. Syncing an Application

Syncing an application applies the desired configuration from Git to the Kubernetes cluster.

Screenshot: Manual Sync Dialog

A sync operation is typically performed when:

* A new application version needs to be deployed.
* Configuration changes need to be applied.
* An application is showing an OutOfSync status.

For production deployments, sync should follow the required change approval process before applying changes.

⸻

5. Sync History and Rollback

The Sync History section provides details about previous application deployments.

Screenshot: Sync History

Developers can review:

* Previous sync operations
* Deployment revisions
* Git commit information
* Deployment timeline

Rollback can be used to restore a previous known working application version when required.

⸻

6. Application Events and Logs

The Events and Logs sections help troubleshoot application issues.

Screenshot: Events / Logs View

Events provide information about Kubernetes resource activity, such as:

* Deployment failures
* Pod scheduling issues
* Resource health problems

Logs provide application runtime information that can help identify application-level issues.
