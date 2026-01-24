# Deploy to all clusters
vim apps/base/myapp.yaml
git add . && git commit -m "Deploy myapp" && git push

# Customize per cluster
vim apps/us-west-2/kustomization.yaml
git add . && git commit -m "us-west-2 specific config" && git push

# Force immediate sync
flux --context us-west-2 reconcile kustomization apps --with-source

# Check what Flux has deployed
flux --context us-west-2 get kustomizations
