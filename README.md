# jupyterhub-ci

One-time-setup:
`alias awsu="awsudo -d 3600 $ADMIN_ARN"`

Run the playbook:
`awsu ansible-playbook get-vars.yml setup-jupyterhub.yml -i hosts.<env>`
