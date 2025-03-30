# Gitea Deployment Assignment

This repository contains the configuration and deployment files for a Gitea instance with MySQL persistence, deployed on Kubernetes.

## Access Details

### Gitea Instance
- **Public URL (Ngrok)**:  
  [https://arriving-humorous-earwig.ngrok-free.app](https://arriving-humorous-earwig.ngrok-free.app)  
  *(Note: Ngrok free tier expires after 2 hours)*

- **Local Access (NodePort)**:  
  `http://localhost:30001` (when running in Codespaces)

### Repository
- **Assignment Submission Repo**:  
  [https://arriving-humorous-earwig.ngrok-free.app/root/assignment-submission](https://arriving-humorous-earwig.ngrok-free.app/root/assignment-submission)

### Admin Credentials
Username: root
Password: Ajay@123456


## Deployment Steps

1. **Prerequisites**:
   - Kubernetes cluster (run in GitHub Codespaces)
   - Helm installed

2. **Deploy MySQL**:
   ```bash
   kubectl apply -f mysql.yaml

3. **Deploy Gitea**:

helm install gitea gitea-charts/gitea --values values.yaml

4. **Access Gitea**:

Use the Ngrok/NodePort URLs above

Log in with admin credentials

## Verification

1. **MySQL Persistence**:

Verify data persists after pod restart:

kubectl delete pod -l app=mysql

2. **Public Access**:

Test access via Ngrok URL in incognito mode
