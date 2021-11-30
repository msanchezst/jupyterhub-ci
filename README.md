# jupyterhub-ci

For convenience: `alias awsu="awsudo -d 3600 $ADMIN_ARN"`

Run the playbooks:
```
# setup jupyterhub configurations
awsu ansible-playbook get-vars.yml setup-jupyterhub.yml -i inventories/<env>.<mission>.hosts.yaml

# setup terraform configurations
awsu ansible-playbook get-vars.yml setup-terraform.yml -i inventories/<env>.<mission>.hosts.yaml
```
