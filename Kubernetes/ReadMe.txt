Make sure you have the following installed:
Minikube (required)
Docker (required)
kubectl (Kubernetes CLI)
Kind (Kubernetes in Docker)
step 1: Install Docker Desktop(optional)
https://www.docker.com/products/docker-desktop/

step 2: Install Minikube
On Linux:
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo install minikube-linux-amd64 /usr/local/bin/minikube

Step 3: Start Minikube
This automatically sets up a single-node Kubernetes cluster locally. You can specify the driver (e.g., Docker or VirtualBox):
minikube start
minikube start --driver=docker

Step 4: Check the Cluster
kubectl get nodes

Step 5: Deploy an App
kubectl create deployment nginx --image=nginx
kubectl expose deployment nginx --port=80 --type=NodePort

Step 6: Access the App
minikube service nginx --url
This command gives you a URL you can open directly in your browser.

Step 7: Optional - Dashboard
This launches the Kubernetes Dashboard in your browser!
minikube dashboard


Step 8: Stop/Delete Cluster
minikube stop
minikube delete