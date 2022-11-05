
```
kubectl get nodes
kubectl get nodes -o wide
kubectl describe pod <podname>
```

## Create a pod

```
#If kubernetes version is latest then only run below  (without generator tag)
kubectl run e2esa-pod01 --image nginx:latest
```

# Debug pod issue
```
kubectl describe pod <podname>
# check the event section after running destribe on any k8s object for any failure or success
```

# List EKS Clusters
```
eksctl get clusters --region [region]
eksctl get clusters --region us-east-1
```

# Capture Node Group name
```
eksctl get nodegroup --cluster=e2esa-demo-eks-cluster --region us-east-1
```

# Delete Node Group
```
eksctl delete nodegroup --cluster=<clusterName> --name=<nodegroupName>  --region [region]
eksctl delete nodegroup --cluster=eksdemo1 --name=eksdemo1-ng-public1 --region us-east-1
```
  
# Delete Cluster
```
eksctl delete cluster <clusterName> --region [region]
eksctl delete cluster eksdemo1 --region us-east-1
```