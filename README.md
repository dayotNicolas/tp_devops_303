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
$ kubectl get pods
NAME                                                     READY   STATUS             RESTARTS        AGE
alertmanager-prometheus-kube-prometheus-alertmanager-0   2/2     Running            0               39m
app-7cdc5ff459-p6tlg                                     1/1     Running            0               128m
app-7cdc5ff459-pn22w                                     1/1     Running            0               3h3m
app-7cdc5ff459-tpj4l                                     1/1     Running            0               128m
hello-world-7dcdb86496-g725x                             1/1     Running            0               128m
hello-world-7dcdb86496-lqjrv                             1/1     Running            0               128m
hello-world-7dcdb86496-xbh9k                             1/1     Running            0               128m
prometheus-grafana-c8787f89b-5tq8c                       1/2     CrashLoopBackOff   13 (82s ago)    41m
prometheus-kube-prometheus-operator-86d499db8f-qlsqp     0/1     CrashLoopBackOff   9 (86s ago)     41m
prometheus-kube-state-metrics-58c5cd6ddb-67q8s           1/1     Running            12 (84s ago)    41m
prometheus-prometheus-kube-prometheus-prometheus-0       1/2     CrashLoopBackOff   8 (4m42s ago)   39m
prometheus-prometheus-node-exporter-hbgrb                1/1     Running            16              41m
redis-6d44c9d869-ggtk8                                   1/1     Running            0               128m
```
:D