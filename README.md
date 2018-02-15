# grakn-kubernetes-cluster

## spawn cluster
kubectl create -f grakn-service.yaml

kubectl create -f grakn-statefulset.yaml

## check grakn status
kubectl exec -ti grakn-0 -- ./grakn server status

## cluster scaling
kubectl scale --replicas=3 statefulset/grakn
