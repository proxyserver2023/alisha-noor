# alisha-noor

An online boutique which empowers women to embrace their inner beauty

# Local development setup

## Pre-requisites

- Docker for desktop
- kubectl
- kind

## Local Cluster

```
kind create cluster --config ./kind-config.yaml
```

```
skaffold run
```

## Architecture

**Online Boutique** is composed of several microservices written in different
languages that talk to each other over REST.

| Service                   | Language | Description                                                                                       |
| ------------------------- | -------- | ------------------------------------------------------------------------------------------------- |
| [frontend](/src/frontend) | React    | The frontend portion.                                                                             |
| [apigw](/src/apigw)       | Go       | API Gateway. Does not require signup/login and generates session IDs for all users automatically. |
