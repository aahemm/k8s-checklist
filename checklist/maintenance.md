**kubelet** 
- approve kubelet CSRs

## Backups 
- `/etc/kubernetes/pki/{ca.crt,ca.key}` 

## Upgrades
etcd: 
- after upgrade checks: 
  - etcd commands/endpoints for healthcheck 
  - check namespaces, nodes, rook-ceph, traefik, services in platform and tools
    