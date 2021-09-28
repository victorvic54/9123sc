## A2_code

### Setup Kubernetes:
- Install Docker Desktop
- Sign in to your account
- Go to Docker Desktop and enables Kubernetes checkbox
- Restart Docker Desktop

### Setup services through kubernetes:
Step 1: apply the yaml under `manifest` directory
```
>>> kubectl apply -f ./manifest
```

Step 2: Ensure deployment are up running
```
>>> kubectl get deployment

NAME             READY   UP-TO-DATE   AVAILABLE   AGE
my-app-service   1/1     1            1           5m22s
```

Step 3: Creating a service:
```
>>> kubectl expose deployment my-app-service --type=LoadBalancer --port=3000 --target-port=3000
```

You can view your service at:
```
http://localhost:3000/
```