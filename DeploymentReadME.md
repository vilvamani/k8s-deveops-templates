## Jenkins Deployment

kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/jenkins/jenkins-serviceaccount.yaml

kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/jenkins/blue/jenkins-persistentvolume.yaml

kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/jenkins/blue/jenkins-persistentvolumeclaim.yaml

kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/jenkins/blue/jenkins-deployment.yaml

kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/jenkins/jenkins-service.yaml

## SonarQube Deployment

kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonarqube/sonarqube-secrets.yaml

kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonarqube/blue/postgres-persistentvolume.yaml

kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonarqube/blue/postgres-persistentvolumeclaim.yaml

kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonarqube/blue/postgres-deployment.yaml

kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonarqube/blue/postgres-service.yaml

kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonarqube/blue/sonarqube-persistentvolume.yaml

kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonarqube/blue/sonarqube-persistentvolumeclaim.yaml

kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonarqube/blue/sonarqube-deployment.yaml

kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonarqube/sonarqube-service.yaml

## SonaType Nexus Deployment

kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonatype-nexus/blue/sonatype-nexus-persistentvolume.yaml

kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonatype-nexus/blue/sonatype-nexus-persistentvolumeclaim.yaml

kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonatype-nexus/blue/sonatype-nexus-statefulset.yaml

kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/sonatype-nexus/sonatype-nexus-service.yaml

## InfluxDB Deployment

kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/influxdb/influxdb-configmap.yaml

kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/influxdb/influxdb-secrets.yaml

kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/influxdb/blue/influxdb-serviceaccount.yaml

kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/influxdb/blue/influxdb-persistentvolume.yaml

kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/influxdb/blue/influxdb-persistentvolumeclaim.yaml

kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/influxdb/blue/influxdb-statefulset.yaml

kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/influxdb/influxdb-service.yaml

## Grafana Dashboard Deployment

kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/grafana/grafana-configmap.yaml

kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/grafana/grafana-secrets.yaml

kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/grafana/blue/grafana-persistentvolume.yaml

kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/grafana/blue/grafana-persistentvolumeclaim.yaml

kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/grafana/blue/grafana-deployment.yaml

kubectl apply -f https://raw.githubusercontent.com/vilvamani/k8s-deveops-templates/main/grafana/grafana-service.yaml
