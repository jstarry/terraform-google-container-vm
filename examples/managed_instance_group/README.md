# Managed Instance Group

This example illustrates how to deploy a container to a [managed instance group](https://cloud.google.com/compute/docs/instance-groups/#managed_instance_groups) in GCP. Also includes SSH key configuration, so a user can be provisioned on the fly for future logins.

## Requirements

This example requires that some python libraries be installed, as outlined in `requirements.txt`. Depending on your environment, you should be able to run `pip install -r requirements.txt` to satisfy these requirements.

[^]: (autogen_docs_start)


## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|:----:|:-----:|:-----:|
| credentials_path | The path to a valid service account JSON credentials file | string | - | yes |
| enable_http_health_check | Whether to enable HTTP health checks | string | `true` | no |
| gce_ssh_user | The username to provision with an auto-generated SSH keypair. | string | `user` | no |
| image | The Docker image to deploy to GCE instances | string | - | yes |
| image_port | The port the image exposes for HTTP requests | string | - | yes |
| machine_type | The GCP machine type to deploy | string | - | yes |
| mig_instance_count | The number of instances to run in the managed instance group | string | `2` | no |
| mig_name | The desired name of the Managed Instance Group to deploy | string | `mig-test` | no |
| project_id | The project ID to deploy resource into | string | - | yes |
| region | The GCP region to deploy instances into | string | - | yes |
| subnetwork | The name of the subnetwork to deploy instances into | string | - | yes |
| subnetwork_project | The project ID where the desired subnetwork is provisioned | string | - | yes |
| zone | The GCP zone to deploy instances into | string | - | yes |

## Outputs

| Name | Description |
|------|-------------|
| container |  |
| credentials_path |  |
| http_address |  |
| http_port |  |
| image |  |
| instance_template_link |  |
| ipv4 |  |
| machine_type |  |
| mig_name |  |
| project_id |  |
| region |  |
| restart_policy |  |
| subnetwork |  |
| subnetwork_project |  |
| vm_container_label |  |
| volumes |  |
| zone |  |

[^]: (autogen_docs_end)

## Running

To provision this example, run the following from within this directory:

- `terraform init` to get plugins
- `terraform plan` to dry-run the infrastructure changes
- `terraform apply` to apply the infrastructure changes
- `terraform destroy` to tear down the created infrastructure