# README

## This is a deployment of a web simple calculator with helm on Kubernetes

Commands:

1. Test 
```
helm template calculator-web > all-in-one.yml
```

2. Installation
```
helm install calculator-web-app --generate-name
``

3. Packaging
```
helm package calculator-web-app
```

4. Port-forwading service frontend
```
kubectl port-forward -n calculator-web-app svc/service-frontend-calculator 8000:80
```

5. Port-forwading service backend
```
kubectl port-forward -n calculator-web-app svc/service-backend-calculator 8001:80
```

6. Use the calculator in browser at 
```
http://localhost:8000
```
