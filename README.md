#Setup

- first clone the repository and goto the cloned directory
- run command ```git submodules update --init --recursive```
- install things listed below
  - docker
  - minikube
  - kubernetes (kubectl)
- install ingress-nginx in minikube
- run minikube start
- run minikube ip and note the ip it returns
- run ```eval $(minikube docker-env)```
- add ```[ip-from-minkube posts.com]``` hosts file at ```/etc/hosts```
- go to ```infra/k8s``` directory and run ```kubectl apply -f .```