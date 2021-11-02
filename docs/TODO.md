
*** How can variables be shared between playbooks?
    Have multiple "shells" on top of each playbook that does the variable collection,
    then "includes" the other playbook

## terraform-deploy

Make configs for:
  - backend.conf (x2)
  - $DEPLOYMENT_NAME.tfvars (x2) # https://github.com/spacetelescope/terraform-deploy/blob/main/ephemeral-setup/your-vars.tfvars.template

Execute:
  - init terraform
  - (plan terraform)
  - apply terraform

## jupyterhub-deploy

  - do we want to generate some of the contents of /hub?
  - (Route 53 update)
  - how to handle secrets???
