# helm-chart

##### helm install --name wiki ./confluence --namespace wiki
##### helm del --purge wiki

##### helm install --name jira ./jira --namespace jira
##### helm del --purge jira


###### git config --global user.email "hbstarjason@gmail.com"
###### git config --global user.name "hbstarjason"

###### helm install --name sonarqube stable/sonarqube -f values-sonarqube.yaml --namespace sonarqube
###### helm del --purge sonarqube

###### helm install --name gitlab stable/gitlab -f values-gitlab.yaml --namespace gitlab
###### helm del --purge gitlab

###### helm repo add harbor https://helm.goharbor.io
###### helm install --name harbor harbor/harbor -f values-harbor.yaml --namespace harbor
