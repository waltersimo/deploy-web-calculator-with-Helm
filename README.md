# README

## This is a deployment of a web simple calculator with helm on Kubernetes

---
### A - Import of the repo
```
git clone https://github.com/waltersimo/deploy-web-calculator-with-Helm.git
cd deploy-web-calculator-with-Helm/
```

### B - Customization
You can edit some variable in the path calculator-web-app/values.yml
```
nano calculator-web-app/values.yml
```

### C- Installation and Packaging

1. Test 
```
helm template calculator-web > all-in-one.yml
```

2. Installation
```
helm install calculator-web-app --generate-name
```

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
---

### D- Use the calculator in browser
```
http://localhost:8000
```
