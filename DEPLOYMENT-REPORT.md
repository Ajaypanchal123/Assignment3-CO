# Kubernetes Deployment Report

## 1. Persistent Volumes Verification

@Ajaypanchal123 ➜ /workspaces/Assignment3-CO (main) $ kubectl get pvc
NAME                   STATUS   VOLUME                                     CAPACITY   ACCESS MODES   STORAGECLASS   VOLUMEATTRIBUTESCLASS   AGE
gitea-shared-storage   Bound    pvc-d4cff264-c9ab-4b84-ac8b-b01edb7cc7d6   10Gi       RWO            local-path     <unset>                 35m
mysql-pv-claim         Bound    mysql-pv-volume                            20Gi       RWO            manual         <unset>                 27m
@Ajaypanchal123 ➜ /workspaces/Assignment3-CO (main) $ 
