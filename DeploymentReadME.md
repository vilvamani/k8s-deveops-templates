## Create Namespace for DevOps

```
kubectl create namespace devops
```

## Jenkins Deployment
```
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/jenkins/jenkins-serviceaccount.yaml --namespace devops
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/jenkins/blue/jenkins-pv.yaml --namespace devops
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/jenkins/blue/jenkins-pvc.yaml --namespace devops
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/jenkins/blue/jenkins-deployment.yaml --namespace devops
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/jenkins/jenkins-service.yaml --namespace devops
```

## SonarQube Deployment
```
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonarqube/sonarqube-secrets.yaml --namespace devops
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonarqube/blue/postgres-pv.yaml --namespace devops
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonarqube/blue/postgres-pvc.yaml --namespace devops
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonarqube/blue/postgres-deployment.yaml --namespace devops
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonarqube/blue/postgres-service.yaml --namespace devops
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonarqube/blue/sonarqube-pv.yaml --namespace devops
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonarqube/blue/sonarqube-pvc.yaml --namespace devops
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonarqube/blue/sonarqube-deployment.yaml --namespace devops
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonarqube/sonarqube-service.yaml --namespace devops
```

## SonaType Nexus Deployment
```
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonatype-nexus/blue/sonatype-nexus-pv.yaml --namespace devops
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonatype-nexus/blue/sonatype-nexus-pvc.yaml --namespace devops
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonatype-nexus/blue/sonatype-nexus-statefulset.yaml --namespace devops
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonatype-nexus/sonatype-nexus-service.yaml --namespace devops
```


> **Note:** Get the Nexus admin user password from **nexus-data/admin.password** file inside conatiner.

## InfluxDB Deployment
```
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/influxdb/influxdb-configmap.yaml --namespace devops
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/influxdb/influxdb-serviceaccount.yaml --namespace devops
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/influxdb/blue/influxdb-pv.yaml --namespace devops
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/influxdb/blue/influxdb-pvc.yaml --namespace devops
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/influxdb/blue/influxdb-statefulset.yaml --namespace devops
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/influxdb/influxdb-service.yaml --namespace devops
```

> **Note:** Login into Influxdb Conatiner and Create **influxdb** to store jenkins job status

> CREATE DATABASE influxdb

## Grafana Dashboard Deployment
```
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/grafana/grafana-configmap.yaml --namespace devops
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/grafana/grafana-secrets.yaml --namespace devops
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/grafana/blue/grafana-pv.yaml --namespace devops
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/grafana/blue/grafana-pvc.yaml --namespace devops
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/grafana/blue/grafana-deployment.yaml --namespace devops
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/grafana/grafana-service.yaml --namespace devops
```

> Install plugins in Grafana

- grafana-cli plugins install grafana-kubernetes-app
- grafana-cli plugins install grafana-piechart-panel
- grafana-cli plugins install btplc-trend-box-panel

> Import the grafana dashboard 10557
