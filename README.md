# Deployment do Guess Game com o K8S

Repositório contendo a aplicação:  
[GitHub](https://github.com/marcosparreiras/guess_game)

## Instruções para a execução

```sh
kubectl apply -f db-secret.yaml
kubectl apply -f db-deployment.yaml
kubectl apply -f db-svc.yaml
kubectl apply -f backend-deployment.yaml
kubectl apply -f backend-hpa.yaml
kubectl apply -f backend-svc.yaml
kubectl apply -f frontend-deployment.yaml
```

Acesse a aplicação no `localhost:3000`

## Instruções para limpar o embiente

```sh
kubectl delete -f frontend-deployment.yaml
kubectl delete -f backend-svc.yaml
kubectl delete -f backend-hpa.yaml
kubectl delete -f backend-deployment.yaml
kubectl delete -f db-svc.yaml
kubectl delete -f db-deployment.yaml
kubectl delete -f db-secret.yaml
```
