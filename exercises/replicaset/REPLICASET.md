# ReplicaSet 

It's main purpose is to maintain a stable set of replica Pods running at any given time. 

Some of the commands that are used here to create and explore PODS are:

- Create ReplicaSet

```
kubectl create -f rc-definition.yaml
```

- Get ReplicaSet
```
kubectl get replicaset
```

- Describe Pods
```
kubectl describe replicaset
```


## Testing
Make sure that ReplicaSet is running and configured properly.

To test out if the ReplicaSet is working as expected, use the pod-definition file available [here](test/pod-definition.yaml) to create a pod with label `backend`.

Now, when you run get pods command. You will notice that the pod that you just created is in terminating state which verifies the functionality of our ReplicaSet. 

