# Prometheus for Metrics

- give permissions for read
- build from this directory
- create the app and expose the app

```
oc login
oc adm policy add-cluster-role-to-user cluster-reader system:serviceaccount:mydemo:default
oc new-build --binary --name=prometheus
oc start-build prometheus --from-dir=. --follow
oc new-app prometheus
oc expose service prometheus
```
