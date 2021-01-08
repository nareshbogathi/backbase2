# - Create a Helm chart that deploys the following:
## - Jenkins server
###  	- Jenkins should be exposed to the internet
###   	- Create a pipeline using jenkinsfile that builds a docker image to run a sample war 


Prerequisites
Helm command line interface
If you don’t have Helm command line interface installed and configured locally, see the sections below to Install Helm and Configure Helm.

Install Helm
To install Helm CLI, follow the instructions from the Installing Helm page.

Configure Helm
Once Helm is installed and set up properly, add the Jenkins repo as follows:
'''
$ helm repo add jenkinsci https://charts.jenkins.io
$ helm repo update
'''
The helm charts in the Jenkins repo can be listed with the command:
'''
$ helm search repo jenkinsci
'''
