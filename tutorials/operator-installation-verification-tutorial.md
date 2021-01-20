---
title: Knative Operator Installation Verification Tutorial
description: Check Operator Deployment Status
---

### Check the Knative Operator 

After installation, verify that your operator is installed successfully by executing the below command.

```execute
kubectl get csv -n operators
```

You should see a similar output as below.

```output
NAME                        DISPLAY               VERSION   REPLACES                    PHASE
knativeoperator.0.37.0   Knative Operator   0.37.0    knativeoperator.0.32.0   Succeeded
```

**Please wait till `PHASE` status will be `Succeeded` and then proceed further.**

After the installation is successful , you can check your operator's pods by executing the below command.

```execute
kubectl get pods -n operators
```

You should see a pod starting with 'knative-operator' with Ready value '1/1' and Status 'Running' like the output below.

```output
NAME                                   READY   STATUS    RESTARTS   AGE
knative-operator-6f7589ff7f-hswnz   1/1     Running   0          6m48s
```

