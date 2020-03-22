# Imperative Commands

Using the kubectl run command can help in generating a YAML template. 
And sometimes, you can even get away with just the kubectl run command without having to create a YAML file at all. 
For example, if you were asked to create a pod or deployment with specific name and image you can simply run the kubectl run command.

Use the below set of commands and try the previous practice tests again, but this time try to use the below commands instead of YAML files.
Try to use these as much as you can going forward in all exercises

Reference (Bookmark this page for exam. It will be very handy):

https://kubernetes.io/docs/reference/kubectl/conventions/


## Create an NGINX Pod

```bash
kubectl run --generator=run-pod/v1 nginx --image=nginx
```


## Generate POD Manifest YAML file (-o yaml). Don't create it(--dry-run)

```bash
kubectl run --generator=run-pod/v1 nginx --image=nginx --dry-run -o yaml
```

```bash
 kubectl run nginx --image=busybox --generator=run-pod/v1 --dry-run
```

## Create a deployment

```bash
kubectl create deployment --image=nginx nginx
```

## Generate Deployment YAML file (-o yaml). Don't create it(--dry-run)

```bash
kubectl create deployment --image=nginx nginx --dry-run -o yaml
```

## Generate Deployment YAML file (-o yaml). Don't create it(--dry-run) with 4 Replicas (--replicas=4)

```bash
kubectl create deployment --image=nginx nginx --dry-run -o yaml > nginx-deployment.yaml
```

Save it to a file, make necessary changes to the file (for example, adding more replicas) and then create the deployment.
