# K3s Fleet GitOps

GitOps repository managing 5 k3s clusters with Flux.

## Clusters
- us-west-2 (192.168.2.200)
- us-east-1 (192.168.2.201)
- eu-west-1 (192.168.2.202)
- ap-southeast-1 (192.168.2.203)
- ap-northeast-1 (192.168.2.204)

## Structure
- `clusters/` - Flux configuration per cluster
- `infrastructure/` - Shared infrastructure (monitoring, ingress, etc.)
- `apps/` - Application deployments
