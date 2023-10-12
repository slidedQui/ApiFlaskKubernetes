# Requisitos
kubectl: https://kubernetes.io/es/docs/tasks/tools/ 
Minikube: https://minikube.sigs.k8s.io/docs/start/

# Pasos de ejecucion
minikube docker-env
& minikube -p minikube docker-env --shell powershell |Invoke-Expression
Docker build . -t flask-api
kubectl apply -f flaskapi-deployment.yml
minikube service flask-service