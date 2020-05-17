## Deployments

A deployment provides a declarative updates to pods and ReplicaSet.

Following are the use case for deployments:
1. Create a rolling update - update to a new version of the image
2. Rollback the update - revert the new version deployment changes
3. Pause the deployment
4. Scale up deployment

Commonly used command with deployments:

- Create Deployment

```
> kubectl create -f deployment-definition.yaml
```


- Get Deployment

```
> kubectl get deployment
```

- Describe deployment
```
> kubectl describe deployment
```

- Rollout a new deployment
```
> kubectl apply -f deployment-definition.yml --record
```

Passing the record flag to apply will record the command used to create a version of the deployment

- Deployment Status Check
```
> kubectl rollout status deployment/deploy-backend
```

- History of the Deployment Rollout
```
> kubectl rollout history deployment/deploy-backend
```

This will return with a list of rollout revisions done for a given deployment.

- Rollback a deployment
```
> kubectl rollout undo deployment/deploy-backend
```
This will rollback to the previous version of the deployment