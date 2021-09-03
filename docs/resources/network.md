---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "eventstorecloud_network Resource - terraform-provider-eventstorecloud"
subcategory: ""
description: |-
  Manages VPC (network) resources in Event Store Cloud
---

# eventstorecloud_network (Resource)

Manages VPC (network) resources in Event Store Cloud

## Example Usage

```terraform
resource "eventstorecloud_project" "example" {
  name = "Example Project"
}

resource "eventstorecloud_network" "example" {
  name = "Example Network"

  project_id = eventstorecloud_project.example.id

  resource_provider = "aws"
  region            = "us-west-2"
  cidr_block        = "172.21.0.0/16"
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- **cidr_block** (String) Address space of the network in CIDR block notation
- **name** (String) Human-friendly name for the network
- **project_id** (String) Project ID
- **region** (String) Provider region in which to provision the network
- **resource_provider** (String) Cloud Provider in which to provision the network.

### Optional

- **id** (String) The ID of this resource.

