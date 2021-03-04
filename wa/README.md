
## Installation

```bash
# Dry Run
$> helm -n <NAMESPACE> install --dry-run <REL_NAME> -f ./general/values.yaml ./general 

# Chart installation
$> helm -n <NAMESPACE> install <REL_NAME> -f ./general/values.yaml ./general 

# Release Upgrade
$> helm -n <NAMESPACE> upgrade <REL_NAME> -f ./general/values.yaml ./general 

# Uninstall
$> helm -n <NAMESPACE> uninstall <REL_NAME>
```


## Checks

### Deployments
✅ Master deployment have only own Secrets and ConfigMap.
✅ Each Worker should share global image and imagePullSecrets.
✅ Each Worker have own Secrets and Global Secrets.
✅ Each Worker have own ConfigMap and Global ConfigMap.
✅ Each Worker should get resource from WorkerTemplate.
✅ If we doesn't supply WorkerTemplate then it takes Master deployment resources.
✅ Each Worker has own probes.
✅ Master has own probes.
✅ Whenever ConfigMap or Secret change Hash should be change of Master and worker.
✅ Each Worker has own commands and args.
✅ Master has own commands and args.

### Services
✅ Master has ClusterIP services.

### ConfigMap
✅ Each Worker have own ConfigMap.

### Secrets
✅ Each Worker have own Secrets.

### Ingress
✅ Ingress created (In k3s )




