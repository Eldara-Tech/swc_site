---
title: Usage
layout: default
---

## swarmcli Usage

### List nodes

```bash
$ swarmctl nodes
ID    HOST    STATUS  AVAIL  MANAGER
1     node1   Ready   Active  Yes
2     node2   Ready   Active  No
```

### List services

```bash
$ swarmctl services
NAME      REPLICAS  IMAGE
web       3/3       nginx:alpine
db        1/1       postgres:14
```

### Inspect service

```bash
$ swarmctl inspect service web
Name: web
Image: nginx:alpine
Replicas: 3
```
