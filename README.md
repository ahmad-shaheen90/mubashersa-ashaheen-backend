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
   <img width="860" alt="Screenshot 2025-04-16 at 12 45 02 AM" src="https://github.com/user-attachments/assets/814614a9-8432-4446-983d-42d77a3990ab" />
   
9. Apply Kubernetes Manifests: "kubectl apply -f k8s/"
10. Then to access the application run "minikube service nodejs-service --url" command to get the URL.
    <img width="668" alt="Screenshot 2025-04-16 at 1 13 28 AM" src="https://github.com/user-attachments/assets/bc29859b-6a97-4fce-8233-51dfd2dac9d7" />

12. Copy the URL and paste in your browser.
    <img width="1435" alt="Screenshot 2025-04-16 at 12 42 21 AM" src="https://github.com/user-attachments/assets/2968246b-4b0c-421e-9084-3570ef785dfd" />
    
