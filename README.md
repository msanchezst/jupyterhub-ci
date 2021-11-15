# jupyterhub-ci

For convenience: `alias awsu="awsudo -d 3600 $ADMIN_ARN"`

Run the playbooks:
```
# setup jupyterhub configurations
awsu ansible-playbook get-vars.yml setup-jupyterhub.yml -i hosts.<env>

# setup terraform configurations
awsu ansible-playbook get-vars.yml setup-terraform.yml -i hosts.<env>
```
