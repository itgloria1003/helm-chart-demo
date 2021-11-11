# Steps by step to create a helm chart 

* Create a helm chart from scratch

```
mkdir ./helm-chart-sources 
helm create helm-chart-sources/helm-chart-test
#  Creating helm-chart-sources/helm-chart-test
```

* Lint the chart
As a good habit, helm lint runs a series of tests to verify that
the chart is well-formed:

```
helm lint helm-chart-sources/*
```

* create is the index.yaml file and the command to do that is:
```
cd helm-chart-sources
helm repo index --url https://github.com/itgloria1003/springapp-helm-chart/ .
```

* push to git repo (GitHub) (_ditto_) 

* Configure the “helm-chart” repository as a Github pages site




---
# Reference : 
https://medium.com/@mattiaperi/create-a-public-helm-chart-repository-with-github-pages-49b180dbb417
