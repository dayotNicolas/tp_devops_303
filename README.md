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
:D