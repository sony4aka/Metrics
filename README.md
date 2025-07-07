Установка Прометей и Граффана
helm install stack prometheus-community/kube-prometheus-stack -f kubernetes/prometheus.yaml
Поды сервиса метрик и сервис монитора
kubectl apply -f kubernetes/service-metrics.yaml -f kubernetes/service-monitor.yaml
