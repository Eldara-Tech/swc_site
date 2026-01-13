---
title: Install
layout: default
---

## Install swarmcli

### Prerequisites

- Docker (with Swarm mode)
- Go (optional, for building from source)

### Install from source

```bash
git clone https://github.com/Eldara-Tech/swarmcli.git
cd swarmcli
go build -o swarmctl ./cmd/swarmctl
sudo mv swarmctl /usr/local/bin/
```

### Docker image (if provided)

```bash
docker pull eldara-tech/swarmcli:latest
docker run --rm -it --network host eldara-tech/swarmcli swarmctl nodes
```
