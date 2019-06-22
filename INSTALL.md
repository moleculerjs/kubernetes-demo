# Minikube

https://kubernetes.io/docs/tasks/tools/install-minikube/

```
curl -Lo minikube https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64 && chmod +x minikube && sudo cp minikube /usr/local/bin/ && rm minikube
```

# Kubectl
https://kubernetes.io/docs/tasks/tools/install-kubectl/

```
sudo snap install kubectl --classic
```

or 

```
sudo apt-get update && sudo apt-get install -y apt-transport-https
curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -
echo "deb https://apt.kubernetes.io/ kubernetes-xenial main" | sudo tee -a /etc/apt/sources.list.d/kubernetes.list
sudo apt-get update
sudo apt-get install -y kubectl
```

# Minikube Quick Start

Start a cluster by running:

`minikube start`

_Runs the Kubernetes components on the host and not in a VM. Using this driver requires Docker (docker install) and a Linux environment_
`minikube start --vm-driver=none`

Enable Ingress:

`minikube addons enable ingress`

Get IP of cluster:

`minikube ip`

Access Kubernetes Dashboard within Minikube:

`minikube dashboard`

Once started, you can interact with your cluster using `kubectl`, just like any other Kubernetes cluster. For instance, starting a server:

`kubectl run hello-minikube --image=k8s.gcr.io/echoserver:1.4 --port=8080`

Exposing a service as a NodePort

`kubectl expose deployment hello-minikube --type=NodePort`

minikube makes it easy to open this exposed endpoint in your browser:

`minikube service hello-minikube`

Start a second local cluster:

`minikube start -p cluster2`

Stop your local cluster:

`minikube stop`

Delete your local cluster:

`minikube delete`

To work with the Docker daemon on your Mac/Linux host, use the docker-env command in your shell:
`eval $(minikube docker-env)`
`docker ps`