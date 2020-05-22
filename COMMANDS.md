# COMMANDS

## Pods
Following are the pod related commands that can come in handy

1. If you want to copy the definition of the existing pod into a new file
```
> kubectl get pod <pod-name> -o yaml > <name-of-the-new-definition-file>
````

2. Directly edit and apply the changes to a pod
```
> kubectl edit pod <pod-name>
```