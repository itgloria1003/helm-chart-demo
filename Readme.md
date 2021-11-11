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
helm package helm-chart-sources/*
helm repo index --url https://github.com/itgloria1003/helm-chart-demo/ .
```

* push to git repo (GitHub) (_ditto_) 

* Configure the “helm-chart” repository as a Github pages site
    - publish the contents of our git repository (public access) as Github pages. 
    - go back to your browser, in the “settings” section of your git repository, scroll down to Github Pages section and configure it as follow:

* add the helm repo (to local kind cluster), for spinnker need to add the repo using the halyard command)
```
helm repo add gloria-helm-chart https://itgloria1003.github.io/helm-chart-demo/
```

* Test the Helm chart repository
helm search test

---
# Reference : 
https://medium.com/@mattiaperi/create-a-public-helm-chart-repository-with-github-pages-49b180dbb417
