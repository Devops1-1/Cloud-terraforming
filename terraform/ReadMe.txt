1.Execute below commands
terraform init
terraform plan
terraform apply

2.Get your kubeconfig to connect to the AKS cluster
az aks get-credentials --resource-group aks-rg --name aks-cluster
kubectl get nodes

3.Deploy your Kubernetes workloads
kubectl apply -f your-ingress-controller.yaml(example)



4.Test your ingress / services
kubectl get svc -n ingress-nginx

5.Cleanup when done
terraform destroy

