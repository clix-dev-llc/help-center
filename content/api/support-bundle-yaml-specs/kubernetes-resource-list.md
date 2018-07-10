---
categories:
- support-bundle-yaml-specs
date: 2018-01-17T23:51:55Z
description: Collect a list of resources managed by the cluster
index: docs
title: kubernetes.resource-list
weight: "100"
gradient: "purpleToPink"
---

## kubernetes.resource-list

Collect a list of resources managed by the cluster


```yaml
specs:
  - kubernetes.resource-list:
      output_dir: /kubernetes/resources/deployments
      namespace: default
      kind: deployments
```

```yaml
specs:
  - kubernetes.resource-list:
      output_dir: /kubernetes/resources/services
      kind: svc
```


### Required Parameters


- `kind` - The Kubernetes resource kind, as would be passed to `kubectl get`



### Optional Parameters


- `namespace` - The Kubernetes namespace


- `resource_list_options` - An instance of metav1.ListOptions



### Outputs

    
- `resource.json` - Logs pulled from Kubernetes pod. Kubernetes pulls logs from stdout/stderr into one output file. If a label selector is provided, it will create multiple log files following the same format.


<br>
{{< note title="Shared Parameters" >}}
This spec also inherits all of the required and optional [Shared Parameters](/api/support-bundle-yaml-specs/shared/)
{{< /note >}}

    