
# Kubernetes Example Probe

![image](https://user-images.githubusercontent.com/3519706/96459618-fc8da600-122a-11eb-9d8d-e07734df1a70.png)

## [](https://github.com/OktaySavdi/kubernetes_probe)Tools & technologies used

1.  Docker
2. Kubernetes

## [](https://github.com/OktaySavdi/kubernetes_probe) Required

-   Docker
-   Kubernetes
-   Ingress Controller

-   `initialDelaySeconds`: Number of seconds after the container has started before liveness or readiness probes are initiated. Defaults to 0 seconds. Minimum value is 0.

-   `periodSeconds`: How often (in seconds) to perform the probe. Default to 10 seconds. Minimum value is 1.

-   `timeoutSeconds`: Number of seconds after which the probe times out. Defaults to 1 second. Minimum value is 1.

-   `successThreshold`: Minimum consecutive successes for the probe to be considered successful after having failed. Defaults to 1. Must be 1 for liveness. Minimum value is 1.

-   `failureThreshold`: When a probe fails, Kubernetes will try  `failureThreshold`  times before giving up. Giving up in case of liveness probe means restarting the container. In case of readiness probe the Pod will be marked Unready. Defaults to 3. Minimum value is 1.

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
