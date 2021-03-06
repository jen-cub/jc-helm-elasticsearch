# Planet-4 Helm chart Elastic Search configuration

## Ingredients:
-   kubectl [https://kubernetes.io/docs/tasks/tools/install-kubectl/](https://kubernetes.io/docs/tasks/tools/install-kubectl/)
-   helm client [https://docs.helm.sh/using_helm/](https://docs.helm.sh/using_helm/)
-   an accessible Kubernetes cluster running Helm Tiller

## Preparation:

```
RELEASE=<my-release> NAMESPACE=<my-namespace> make
```

## Dining:

To access Elasticsearch from within your cluster, use:

`$RELEASE-elasticsearch-client.$NAMESPACE.svc.cluster.local:9200`

To connect from outside the cluster:

```
make port &
curl http://localhost:9200/_cat/health
```

## Cleaning up:

```
make clean
```
