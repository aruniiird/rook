# Monitoring ceph storage with ceph-mixins

---

## Overview

Currently, rook deploys ceph storage but not ceph monitoring. It can be deployed manually using documented steps. But still, it lacks Prometheus Alerts and Recording Rules that is useful in easy monitoring of ceph storage.

This is where **ceph-mixins** comes in. Ceph-mixins defines a minimalistic approach to package together the ceph storage specific prometheus alerts, recording rules and grafana dashboards, in a simple and platform agnostic way.

Rook can use ceph-mixins as the default solution for monitoring ceph storage.

## Design

---

### Responsibilities

### Deployment

1. Fetching latest resources from ceph-mixins
2. Building deployment yaml
3. Deploying
   1. In Kubernetes
   2. In Openshift