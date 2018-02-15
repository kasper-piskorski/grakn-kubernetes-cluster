# grakn-kubernetes-cluster

## spawn cluster
`kubectl create -f grakn-service.yaml`

`kubectl create -f grakn-statefulset.yaml`

## check grakn status
`kubectl exec -ti grakn-0 -- ./grakn server status`

## cluster scaling
`kubectl scale --replicas=<NO_OF_NODES> statefulset/grakn`

## use local grakn docker image (minikube)
`eval $(minikube docker-env)`

`cd GRAKN_IMAGE_DIR`

`docker build -t grakn .`

=> update `grakn-statefulset.yaml` image line accordingly
