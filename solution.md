
1. Provision cluster
```shell
terraform apply
```
2. Add cluster config to local kubeconfig
```shell
aws eks --region $(terraform output -raw region) update-kubeconfig --name $(terraform output -raw cluster_name)
```