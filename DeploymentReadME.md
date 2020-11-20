## Jenkins Deployment
```
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/jenkins/jenkins-serviceaccount.yaml
```
```
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/jenkins/blue/jenkins-pv.yaml
```
```
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/jenkins/blue/jenkins-pvc.yaml
```
```
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/jenkins/blue/jenkins-deployment.yaml
```
```
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/jenkins/jenkins-service.yaml
```

## SonarQube Deployment
```
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonarqube/sonarqube-secrets.yaml
```
```
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonarqube/blue/postgres-pv.yaml
```
```
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonarqube/blue/postgres-pvc.yaml
```
```
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonarqube/blue/postgres-deployment.yaml
```
```
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonarqube/blue/postgres-service.yaml
```
```
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonarqube/blue/sonarqube-pv.yaml
```
```
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonarqube/blue/sonarqube-pvc.yaml
```
```
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonarqube/blue/sonarqube-deployment.yaml
```
```
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonarqube/sonarqube-service.yaml
```

## SonaType Nexus Deployment
```
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonatype-nexus/blue/sonatype-nexus-pv.yaml
```
```
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonatype-nexus/blue/sonatype-nexus-pvc.yaml
```
```
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonatype-nexus/blue/sonatype-nexus-statefulset.yaml
```
```
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonatype-nexus/sonatype-nexus-service.yaml
```

## InfluxDB Deployment
```
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/influxdb/influxdb-configmap.yaml
```
```
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/influxdb/influxdb-secrets.yaml
```
```
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/influxdb/influxdb-serviceaccount.yaml
```
```
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/influxdb/blue/influxdb-pv.yaml
```
```
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/influxdb/blue/influxdb-pvc.yaml
```
```
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/influxdb/blue/influxdb-statefulset.yaml
```
```
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/influxdb/influxdb-service.yaml
```

## Grafana Dashboard Deployment
```
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/grafana/grafana-configmap.yaml
```
```
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/grafana/grafana-secrets.yaml
```
```
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/grafana/blue/grafana-pv.yaml
```
```
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/grafana/blue/grafana-pvc.yaml
```
```
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/grafana/blue/grafana-deployment.yaml
```
```
kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/grafana/grafana-service.yaml
```
