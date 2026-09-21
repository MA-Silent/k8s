```sh
kubectl -n longhorn-system port-forward svc/longhorn-frontend 8080:80
```

```sh
sops --encrypt --in-place --config=./clusters/home/.sops.yaml encrypted-secrets/home/<secret>.yaml 
```