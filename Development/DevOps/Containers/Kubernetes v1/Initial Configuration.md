###### Config kubectl:
- `sudo apt-get install curl -y`
- `curl -LO "https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl"`
- `chmod +x ./kubectl`
- `sudo mv ./kubectl /usr/local/bin/kubectl`

###### Config minikube:
- `curl -Lo minikube https://storage.googleapis.com/minikube/releases/v1.12.1/minikube-linux-amd64 \ && chmod +x minikube`
- `sudo install minikube /usr/local/bin/`

###### Config kubectl with minikube:
- Docker: `minikube start --vm-driver=docker
- VirtualBox: `minikube start --driver=virtualbox
#Kubernetes