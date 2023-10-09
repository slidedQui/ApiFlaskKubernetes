# Pasos de ejecucion
minikube docker-env
& minikube -p minikube docker-env --shell powershell |Invoke-Expression
Docker build . -t flask-api
kubectl apply -f flaskapi-deployment.yml
minikube service flask-service