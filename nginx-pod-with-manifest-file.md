# Nginx pod using manifest file

## **nginx example**

- Create the following yml file. Give it name `nginx-pods.yml`

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: nginx-pod
spec:
  containers:
    - name: nginx
      image: nginx
      ports:
        - containerPort: 80
```

**Run the above yml file with following command**

`kubectl apply -f nginx-pods.yml`

Since we don’t have services so only way to check running nginx is to go inside the pod.
Later we will have services created then we will be able to see the running application.

```bash
kubectl exec -it pod/nginx-pod -- /bin/bash
apt-get update
apt-get install curl
curl localhost
```

- Now update the nginx image version to `nginx:1.16` and apply the configuration again.

- **Now create a yml file with wrong container name and show `ErrImagePull`**
