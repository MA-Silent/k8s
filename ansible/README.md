## Load ssh key

```sh
ssh-add ~/.ssh/id_ed25519
```

## adhoc

```sh
ansible -m ping -i inventory.ini all --become --vault-pass-file=~/.vault-pass
```

```sh
ansible all -m ansible.builtin.shell -a 'rm -f /etc/yum.repos.d/Docker*' --become --vault-pass-file=~/.vault-pass -i inventory.ini
```

# Kubernetes Setup

```sh
ansible packages.yaml -i inventory.ini -e run_hosts="kube-X" --vault-pass-file=~/.vault-pass
```

## Manual (ssh)
```sh
kubeadm init --control-plane-endpoint=cluster-endpoint
```