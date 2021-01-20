---
title: Knative Instance Creation tutorial
description: This tutorial explains how create Instances for Knative
---
### Create below yaml to create Custom Resource Definitions for Knative Serving:

```execute
cat <<'EOF' > KnativeServingInstance.yaml
apiVersion: operator.knative.dev/v1alpha1
kind: KnativeServing
metadata:
  name: knative-serving
spec: {}
EOF
```

Execute below command to create Knative Serving instance: 

```execute
kubectl create -f KnativeServingInstance.yaml -n operators
```

You will see the following resources created:

```output
prometheus.monitoring.coreos.com/prometheus created
```

Get the associated Pods:

```execute
kubectl get pods -n operators
```
You will be able to see pods:

```output
NAME                                   READY   STATUS    RESTARTS   AGE
prometheus-operator-6f7589ff7f-qdh9c   1/1     Running   0          102s
prometheus-server-0                    3/3     Running   1          26s
```


