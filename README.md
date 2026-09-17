# ArgoCD Developer UI Walkthrough

## 1. Applications

The Applications page lists the applications managed by ArgoCD. It shows each application's health, sync status, Git repository, and target environment.

**Screenshot:** Application Dashboard

`Healthy` means the resources are running correctly, `Progressing` means a change is being applied or resources are starting, and `Degraded` indicates a problem. `Synced` means the cluster matches Git, while `OutOfSync` means they differ.

## 2. Application Details

Select an application to view its Kubernetes resources, such as deployments, pods, services, and ConfigMaps. The resource tree makes it easy to find unhealthy or failing components.

**Screenshot:** Application Detail / Resource Tree

## 3. Reviewing Changes

The Diff view compares the live Kubernetes state with the desired state in Git. Review it before syncing to confirm changes to images, configuration, environment variables, replicas, or manifests.

**Screenshot:** Diff View

## 4. Syncing

Sync applies the desired Git configuration to the cluster. Use it to deploy a new version, apply configuration changes, or correct an `OutOfSync` application. Production syncs should follow the required approval process.

**Screenshot:** Manual Sync Dialog

## 5. History and Rollback

Sync History shows previous deployments, Git revisions, and their timestamps. If needed, use a previous successful revision to restore a working version.

**Screenshot:** Sync History

## 6. Events and Logs

Use Events to investigate deployment failures, scheduling issues, and unhealthy resources. Use Logs to troubleshoot application runtime errors.

**Screenshot:** Events / Logs View
