# TP Devops 101

Composiiton du duo: *Nicolas Dayot* & *Samuel Adone*
_lien du git_: https://github.com/dayotNicolas/tp_devops_303.git
## 1. Découpage de namespace
```
.
├── namespace_dev
│   ├── app
│   │   ├── configMap.yml
│   │   ├── deployment-app.yml
│   │   ├── ingress-app.yml
│   │   └── service-app.yml
│   ├── quota-mem-cpu.yml
│   └── redis
│       ├── deployment-redis.yml
│       └── service-redis.yml
└── namespace_hello
    └── hello_world
        ├── deployment-hello_world.yml
        ├── ingress-hello_world.yml
        ├── quota-mem-cpu.yml
        └── service-hello_world.yml

```
(en gros) ça ressemble à ça:
```bash=
$ kubectl get namespace
NAME              STATUS   AGE  
default           Active   5h20m
dev               Active   164m
hello             Active   164m
ingress-nginx     Active   5h19m
kube-node-lease   Active   5h20m
kube-public       Active   5h20m
kube-system       Active   5h20m
```



---

![](https://giphy.com/gifs/ending-looney-tunes-the-end-l4pTjOu0NsrLApt0Q)

## 4. Prometheus
```bash
    $ kubectl get service
NAME                                      TYPE        CLUSTER-IP       EXTERNAL-IP   PORT(S)                      AGE
alertmanager-operated                     ClusterIP   None             <none>        9093/TCP,9094/TCP,9094/UDP   49m
app                                       ClusterIP   10.108.228.243   <none>        80/TCP                       5h29m
hello-world                               ClusterIP   10.103.146.51    <none>        80/TCP                       5h27m
kubernetes                                ClusterIP   10.96.0.1        <none>        443/TCP                      5h37m
prometheus-grafana                        ClusterIP   10.110.210.220   <none>        80/TCP                       52m
prometheus-kube-prometheus-alertmanager   ClusterIP   10.110.159.132   <none>        9093/TCP                     52m
prometheus-kube-prometheus-operator       ClusterIP   10.96.239.158    <none>        443/TCP                      52m
prometheus-kube-prometheus-prometheus     ClusterIP   10.110.207.163   <none>        9090/TCP                     52m
prometheus-kube-state-metrics             ClusterIP   10.107.146.175   <none>        8080/TCP                     52m
prometheus-operated                       ClusterIP   None             <none>        9090/TCP                     49m
prometheus-prometheus-node-exporter       ClusterIP   10.103.40.183    <none>        9100/TCP                     52m
redis                                     ClusterIP   10.99.164.159    <none>        6379/TCP                     4h29m
```
:D