# GKE Clusters Module
Dynamic terraform GKEe cluster module code. This module will be called from ../env/dev.tf modules file, by using this module reusable module we will be able to create gke cluster and node pools.

main.tf contains all the resources which will be created while terraform apply, variables.tf file containes all the variables required to create the resources and outputs.tf files for output the attributes of the resources.


## Google cloud resources
* GKE cluster
* Cluster node pool
* Google project service

## Providers
|       NAME        |   Version  | 
|-------------------|------------|
| terraform version |   0.14     |
| gcp provider      |   ~>3.0    |

## Inputs

|       Name        |   Description  |  Type  |  Required    |
|-------------------|----------------|--------|:------------:|
| name |  name of the cluster and prefix of the related resources names | `string` | yes |
| project_id |  Id of the project which holds the components | `string` | yes |
| region | the region to create the vpc network | `string` | yes |
| initial_node_count | initial node count | `string` | no |
| mechine_type | type of gcp virtuval machine | `string` | no | 
| network_link | network link | `string` | yes |
| subnetwork_link | subnetwork_link | `string` | yes |
| service_account | service account email | `string` | yes |

## Outputs

|    Name     |    description   | 
|-------------|:----------------:|
|   endpoint  | google container cluster endpoint |
| master_version| google container cluster master version |