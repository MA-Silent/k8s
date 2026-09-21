```sh
kubectl -n longhorn-system port-forward svc/longhorn-frontend 8080:80
```

## encryption

```sh
gpg --import ./clusters/home/.sops.pub.asc
```

```sh
sops --encrypt --in-place --config=./clusters/home/.sops.yaml encrypted-secrets/home/<secret>.yaml 
```