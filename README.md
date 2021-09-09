# description
kubernertes Jenkins Deployment

# Files collection
- jenkins-namespace.yaml: create the namespace for the jenkins kubernetes resources
- jenkins-volume.yaml: create a persistence volume for jenkins
- jenkins-sa.yaml: create the service account for jenkins pod
- jenkins-values.yaml: jenkins chart configuration

# Install helm chart
```
chart=jenkinsci/jenkins
helm install jenkins -n jenkins -f jenkins-values.yaml $chart
```

# check jenkins controller pod created for the heml chart
```
kubectl logs jenkins-0 -c init
```
