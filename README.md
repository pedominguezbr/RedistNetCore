# RedistNetCore

## Compile Docker images 
```
docker build -t redistnetcore .
docker tag redistnetcore pedominguezbr/redistnetcore:1.0
docker push pedominguezbr/redistnetcore:1.0

# run image
docker run --name redistnetcore_test --rm -t redistnetcore 

# run image settting appsettings.json
docker run --name redistnetcore_test --mount type=bind,source="$(pwd)"/appsettings.json,target=/app/appsettings.json --rm -t redistnetcore
```

## Deploy in Kube 
```
kubectl apply -f ./Deploy-k8s
```