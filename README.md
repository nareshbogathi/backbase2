# - Create a Helm chart that deploys the following:
## - Jenkins server
###  	- Jenkins should be exposed to the internet
###   	- Create a pipeline using jenkinsfile that builds a docker image to run a sample war 


Prerequisites
Helm command line interface
If you don’t have Helm command line interface installed and configured locally, see the sections below to Install Helm and Configure Helm.

Install Helm
To install Helm CLI, follow the instructions from the Installing Helm page.
https://helm.sh/docs/intro/install/

Configure Helm
Once Helm is installed and set up properly, add the Jenkins repo as follows:
```
$ helm repo add jenkinsci https://charts.jenkins.io
$ helm repo update
```
The helm charts in the Jenkins repo can be listed with the command:
```
$ helm search repo jenkinsci
```

### - Create a pipeline using jenkinsfile that builds a docker image to run a sample war 

![alt text](./img/img.png)

```
minikube start
```
```
minikube service list
```
```
brew install helm
```
```
helm repo add bitnami https://charts.bitnami.com/bitnami
```
```
helm install my-release bitnami/jenkins
```

```
NLMB2B16-C61554:tmp nareshbogathi$ helm install my-release bitnami/jenkins
NAME: my-release
LAST DEPLOYED: Sun Jan 10 17:43:38 2021
NAMESPACE: default
STATUS: deployed
REVISION: 1
TEST SUITE: None
NOTES:
** Please be patient while the chart is being deployed **

1. Get the Jenkins URL by running:

** Please ensure an external IP is associated to the my-release-jenkins service before proceeding **
** Watch the status using: kubectl get svc --namespace default -w my-release-jenkins **

  export SERVICE_IP=$(kubectl get svc --namespace default my-release-jenkins --template "{{ range (index .status.loadBalancer.ingress 0) }}{{.}}{{ end }}")
  echo "Jenkins URL: http://$SERVICE_IP/"

2. Login with the following credentials

  echo Username: user
  echo Password: $(kubectl get secret --namespace default my-release-jenkins -o jsonpath="{.data.jenkins-password}" | base64 --decode)
```

http://192.168.64.2:31390

  ![alt text](./img/img1.png)

