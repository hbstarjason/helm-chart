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
# wget https://raw.githubusercontent.com/hbstarjason/helm-chart/master/values-sonarqube.yaml
helm install --name sonarqube stable/sonarqube -f values-sonarqube.yaml --namespace sonarqube
helm del --purge sonarqube
```

```sh
# install gitlab
# wget https://raw.githubusercontent.com/hbstarjason/helm-chart/master/values-gitlab.yaml
helm install --name gitlab stable/gitlab-ce -f values-gitlab.yaml --namespace gitlab
helm del --purge gitlab
```

```sh
# install harbor
# https://github.com/goharbor/harbor-helm
# wget https://raw.githubusercontent.com/hbstarjason/helm-chart/master/values-harbor.yaml
sed -i 's/nfs-client/standard/g'  values-harbor.yaml
helm repo add harbor https://helm.goharbor.io
helm install --name harbor harbor/harbor -f values-harbor.yaml --namespace harbor
```

```sh
# install influxdb
# wget https://raw.githubusercontent.com/hbstarjason/helm-chart/master/values-influxdb-test.yaml
helm install --name influxdb stable/influxdb -f values-influxdb-test.yaml --namespace influxdb
```


```sh
# install spinnaker
# https://github.com/moondev/spinnaker-helm
helm install --name spinnaker ./spinnaker --namespace spinnaker
kubectl get pods --namespace spinnaker

# kubectl get svc deck -n spinnaker -o yaml |sed 's/NodePort/LoadBalancer/' |kubectl replace -f -


# official chart 
# https://hub.helm.sh/charts/stable/spinnaker
# https://github.com/helm/charts/blob/master/stable/spinnaker/README.md

# helm install -n spinnaker stable/spinnaker --namespace spinnaker --timeout 600

# wget https://raw.githubusercontent.com/helm/charts/master/stable/spinnaker/values.yaml
# https://raw.githubusercontent.com/hbstarjason/helm-chart/master/values-spinnaker-test.yaml
# helm install -n spinnaker stable/spinnaker -f values-spinnaker-test.yaml --debug
```
