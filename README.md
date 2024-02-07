# CloudChallenge
This is my submission for the Cloud Ran Challenge

## Kubernetes 
Steps to deploy and expose the hello app with Kubernetes:

0. Start Docker Desktop with a Kubernetes Cluster
1. Go to the ./CloudChallenge directory 
2. Deploy hello app to the cluster with `kubectl apply -f ./Kubernetes/deployment.yaml`
3. Expose the service with `kubectl apply -f ./Kubernetes/service.yaml`
4. Get the port of the Node with `kubectl get service`
5. Test the service with `curl http://localhost:{port}`
6. Once you're done, delete the deployment with `kubectl delete -f ./Kubernetes/`


## Helm 
Steps to deploy the hello app with Helm chart

0. Start Docker Desktop with a Kubernetes Cluster
1. Deploy hello app: `helm install hello-app ./hello-app-chart`
2. Get the port of the Node with `kubectl get service`
3. Test the deployment with `curl http://localhost:{port}`
4. Once you're done, take down the deployment: `helm uninstall hello-app`
