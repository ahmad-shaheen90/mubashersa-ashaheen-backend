# mubashersa-ashaheen-backend

This repo contains a task solution that was done by Ahmad Shaheen for Mubasher.sa.

Task objective: Containerize a Node.js application and deploy it on a local Kubernetes cluster using Minikube.

To run the application on Minikube cluster please follow the below steps:

1. Clone the repo from: https://github.com/ahmad-shaheen90/mubashersa-ashaheen-backend/tree/main
2. Docker engine and Minikube should be installed as a prerequisit.
3. Start Minikube using "minikube start" command.
4. Point the shell to minikube's docker-daemon using "eval $(minikube -p minikube docker-env)" command.
5. From inside the project directory build the docker image using "docker build -t nodejs-app:latest ." command.
6. Load the docker image to Minikube registry to be used from inside Minikube: "minikube image load nodejs-app:latest"
7. To check the image inside Minikube you can use "minikube image ls" command.
8. Apply Kubernetes Manifests: "kubectl apply -f k8s/"
9. Then to access the application run "minikube service nodejs-service --url" command to get the URL.
10. Copy the URL and paste in your browser.
