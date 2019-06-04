# helm-chart

```sh
# config git
git config --global user.email "hbstarjason@gmail.com" && \
git config --global user.name "hbstarjason"
```

```sh
# install confluence
helm install --name confluence ./confluence --namespace confluence
helm del --purge confluence
```

```sh
# install jira
helm install --name jira ./jira --namespace jira
helm del --purge jira
```

```sh
# install sonarqube
helm install --name sonarqube stable/sonarqube -f values-sonarqube.yaml --namespace sonarqube
helm del --purge sonarqube
```

```sh
# install gitlab
helm install --name gitlab stable/gitlab -f values-gitlab.yaml --namespace gitlab
helm del --purge gitlab
```

```sh
# install harbor
helm repo add harbor https://helm.goharbor.io
helm install --name harbor harbor/harbor -f values-harbor.yaml --namespace harbor
```
