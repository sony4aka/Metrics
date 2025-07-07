Установка Прометей и Граффана
helm install stack prometheus-community/kube-prometheus-stack -f kubernetes/prometheus.yaml
Поды сервиса метрик и сервис монитора
kubectl apply -f kubernetes/service-metrics.yaml -f kubernetes/service-monitor.yaml

1.графана 
kubectl port-forward svc/stack-grafana 3000:80
http://localhost:3000/

2.прометеус
kubectl port-forward svc/stack-kube-prometheus-stac-prometheus 9090:9090 -n default
http://localhost:9090/
