# jupyterhub-ci

For convenience: `alias awsu="awsudo -d 3600 $ADMIN_ARN"`

Run the playbooks:
```
# setup jupyterhub configurations
awsu ansible-playbook get-vars.yml setup-jupyterhub.yml -i inventories/<env>.<mission>.hosts.yaml

# setup terraform configurations
awsu ansible-playbook get-vars.yml setup-terraform.yml -i inventories/<env>.<mission>.hosts.yaml

# set up datadog
# must source setup-env for now! This relies on that code because the ansible filter does not work.
awsudo $ADMIN_ARN -i inventories/<env>.<mission>.hosts.yaml setup-datadog
# this may fail if you lack perms to get the datadog API key secret from this account
```
