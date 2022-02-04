# Setup

- first clone the repository and goto the cloned directory
- run command `git submodules update --init --recursive`
- install things listed below
  - docker
  - minikube
  - kubernetes (kubectl)
- install ingress-nginx in minikube
- run minikube start
- run minikube ip and note the ip it returns
- run `eval $(minikube docker-env)`
- add `[ip-from-minkube posts.com]` hosts file at `/etc/hosts`

## Run with kubectl

- go to `infra/k8s` directory and run `kubectl apply -f .`

## Run with skaffold

- make sure docker, minikube kubernetes are installed.
- make sure minikube cluster is running (minikube start).
- run `eval $(minikube docker-env)` # it changes the docker environment to whih minikube cluster is running
- install skaffold on your system
- go to project root dir (in this case micro-blog)
- run `skaffold dev`

## Test

- go to posts.com add some posts and do refresh
- add some comments to post and do refresh
