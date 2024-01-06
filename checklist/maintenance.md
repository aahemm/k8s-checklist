**kubelet** 
- approve kubelet CSRs

**ceph** 
- clean released PVs and their rbd images 
  
## Backups 
- `/etc/kubernetes/pki/{ca.crt,ca.key}` 
- etcd data

## Upgrades
etcd: 
- after upgrade checks: 
  - etcd commands/endpoints for healthcheck 
  - check namespaces, nodes, rook-ceph, traefik, services in platform and tools
  - check some random pod log
    
kube-prometheus-stack:
- after upgrade checks:
  - check if these pods are running: operator, prometheus, alert manager, grafana, node exporter and ksm
  - check prometheus dashboard for targets and rules. including: traefik, ceph, coredns alerts and targets
  - check dashboards in grafana. add new dashboards if they are gone. including: traefik, ceph
  - check alert manager watchdog alert. add silences if they are gone. including: ceph health silences
  - check watchdog external services