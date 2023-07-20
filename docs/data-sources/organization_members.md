---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "lightdash_organization_members Data Source - terraform-provider-lightdash"
subcategory: ""
description: |-
  Lightdash organization member data source
---

# lightdash_organization_members (Data Source)

Lightdash organization member data source

## Example Usage

```terraform
data "lightdash_organization_members" "test" {
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Read-Only

- `id` (String) Data source identifier
- `members` (Attributes List) List of projects. (see [below for nested schema](#nestedatt--members))
- `organization_uuid` (String) Lightdash organization UUID

<a id="nestedatt--members"></a>
### Nested Schema for `members`

Read-Only:

- `email` (String) Lightdash user UUID
- `role` (String) Lightdash user UUID
- `user_uuid` (String) Lightdash user UUID