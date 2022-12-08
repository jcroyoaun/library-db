# library-db

This is a study case on how to approach the container creation and architecture for a Spring Boot app as a DevOps engineer using an nginx reverse proxy to the Java backend and a mariadb for writing data.

This app works in conjunction with repos

* library-backend-api
* library-webserver

1. Library DB should get started first
2. Library Backend API should get started second
3. Lastly, we start Library Webserver


### Step #1 to run Library DB
1. First start minikube on your local by typing
```
minikube start
```

2. Then, run a minikube mount on the data directory from this same repo :
```
cd data
DIR=$(pwd)
minikube mount $DIR:$DIR
```
3. Deploy kubernetes deployment and services
```
kubectl apply -f .
```
