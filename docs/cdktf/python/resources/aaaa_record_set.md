---

<!-- Please do not edit this file, it is generated. -->
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "dns_aaaa_record_set Resource - terraform-provider-dns"
subcategory: ""
description: |-
  Creates an AAAA type DNS record set.
---

# dns_aaaa_record_set (Resource)

Creates an AAAA type DNS record set.

## Example Usage

```python
# DO NOT EDIT. Code generated by 'cdktf convert' - Please report bugs at https://cdk.tf/bug
from constructs import Construct
from cdktf import TerraformStack
#
# Provider bindings are generated by running `cdktf get`.
# See https://cdk.tf/provider-generation for more details.
#
from imports.dns.aaaa_record_set import AaaaRecordSet
class MyConvertedCode(TerraformStack):
    def __init__(self, scope, name):
        super().__init__(scope, name)
        AaaaRecordSet(self, "www",
            addresses=["fdd5:e282:43b8:5303:dead:beef:cafe:babe", "fdd5:e282:43b8:5303:cafe:babe:dead:beef"
            ],
            name="www",
            ttl=300,
            zone="example.com."
        )
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `addresses` (Set of String) The IPv6 addresses this record set will point to.
- `zone` (String) DNS zone the record set belongs to. It must be an FQDN, that is, include the trailing dot.

### Optional

- `name` (String) The name of the record set. The `zone` argument will be appended to this value to create the full record path.
- `ttl` (Number) The TTL of the record set. Defaults to `3600`.

### Read-Only

- `id` (String) The ID of this resource.

## Import

Import is supported using the following syntax:

```shell
# Import using the FQDN.
terraform import dns_aaaa_record_set.www www.example.com.
```

<!-- cache-key: cdktf-0.18.0 input-e351b2d651318b36501b9a8c9b38822b78f62300c58176c5eda249596aa9dc53 -->