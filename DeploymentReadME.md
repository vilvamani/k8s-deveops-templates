## Create Namespace for DevOps

```
kubectl create namespace devops
```

## Jenkins Deployment
```
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/jenkins/jenkins-serviceaccount.yaml
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/jenkins/blue/jenkins-pv.yaml
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/jenkins/blue/jenkins-pvc.yaml
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/jenkins/blue/jenkins-deployment.yaml
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/jenkins/jenkins-service.yaml
```

## SonarQube Deployment
```
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonarqube/sonarqube-secrets.yaml
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonarqube/blue/postgres-pv.yaml
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonarqube/blue/postgres-pvc.yaml
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonarqube/blue/postgres-deployment.yaml
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonarqube/blue/postgres-service.yaml
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonarqube/blue/sonarqube-pv.yaml
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonarqube/blue/sonarqube-pvc.yaml
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonarqube/blue/sonarqube-deployment.yaml
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonarqube/sonarqube-service.yaml
```

## SonaType Nexus Deployment
```
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonatype-nexus/blue/sonatype-nexus-pv.yaml
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonatype-nexus/blue/sonatype-nexus-pvc.yaml
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonatype-nexus/blue/sonatype-nexus-statefulset.yaml
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonatype-nexus/sonatype-nexus-service.yaml
```


> **Note:** Get the Nexus admin user password from **nexus-data/admin.password** file inside conatiner.

## InfluxDB Deployment
```
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/influxdb/influxdb-configmap.yaml
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/influxdb/influxdb-serviceaccount.yaml
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/influxdb/blue/influxdb-pv.yaml
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/influxdb/blue/influxdb-pvc.yaml
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/influxdb/blue/influxdb-statefulset.yaml
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/influxdb/influxdb-service.yaml
```

> **Note:** Login into Influxdb Conatiner and Create **influxdb** to store jenkins job status

> CREATE DATABASE influxdb

## Grafana Dashboard Deployment
```
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/grafana/grafana-configmap.yaml
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/grafana/grafana-secrets.yaml
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/grafana/blue/grafana-pv.yaml
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/grafana/blue/grafana-pvc.yaml
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/grafana/blue/grafana-deployment.yaml
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/grafana/grafana-service.yaml
```

> Install plugins in Grafana

- grafana-cli plugins install grafana-kubernetes-app
- grafana-cli plugins install grafana-piechart-panel
- grafana-cli plugins install btplc-trend-box-panel

> Import the grafana dashboard 10557
