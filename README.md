
# Kubernetes Example Probe

![image](https://user-images.githubusercontent.com/3519706/96459618-fc8da600-122a-11eb-9d8d-e07734df1a70.png)

## [](https://github.com/OktaySavdi/kubernetes_probe)Tools & technologies used

1.  Docker
2. Kubernetes

## [](https://github.com/OktaySavdi/kubernetes_probe) Required

-   Docker
-   Kubernetes
-   Ingress Controller

## [](https://github.com/OktaySavdi/kubernetes_probe) Install

Give execute permission for install.sh
```
kubectl create namespace probe
```
Install example
```
kubectl create -f probe.yml -n probe
```
```
kubectl get po -n probe
kubectl describe po -n probe
```
Call URL
```ruby
curl http://PodIP/health/ready

curl http://PodIP/health/live
```
