---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "fmc_dynamic_object_mapping Resource - terraform-provider-fmc"
subcategory: ""
description: |-
  Resource for Dynamic Object Mapping in FMC
  Example
  An example is shown below:
  hcl
  resource "fmc_dynamic_object" "test" {
    name        = "test"
    object_type = "IP"
    description = "test dynamic object"
  }
  resource "fmc_dynamic_object_mapping" "test" {
    dynamic_object_id = fmc_dynamic_object.test.id
    mappings = "8.8.8.8"
  }
---

# fmc_dynamic_object_mapping (Resource)

Resource for Dynamic Object Mapping in FMC

## Example
An example is shown below: 
```hcl
resource "fmc_dynamic_object" "test" {
  name        = "test"
  object_type = "IP"
  description = "test dynamic object"
}
resource "fmc_dynamic_object_mapping" "test" {
  dynamic_object_id = fmc_dynamic_object.test.id
  mappings = "8.8.8.8"
}
```



<!-- schema generated by tfplugindocs -->
## Schema

### Required

- **dynamic_object_id** (String) ID of dynamic object to be used for mapping
- **mappings** (List of String) List of IPs to be mapped to dynamic object

### Optional

- **id** (String) The ID of this resource.

