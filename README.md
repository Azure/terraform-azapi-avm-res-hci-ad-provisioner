<!-- BEGIN_TF_DOCS -->
# terraform-azurerm-avm-ptn-hci-ad-provisioner

Module to provision azure stack hci ad.

<!-- markdownlint-disable MD033 -->
## Requirements

The following requirements are needed by this module:

- <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) (>= 1.9, < 2.0)

- <a name="requirement_azurerm"></a> [azurerm](#requirement\_azurerm) (~> 4.0)

- <a name="requirement_modtm"></a> [modtm](#requirement\_modtm) (~> 0.3)

- <a name="requirement_random"></a> [random](#requirement\_random) (~> 3.5)

## Resources

The following resources are used by this module:

- [modtm_telemetry.telemetry](https://registry.terraform.io/providers/azure/modtm/latest/docs/resources/telemetry) (resource)
- [random_uuid.telemetry](https://registry.terraform.io/providers/hashicorp/random/latest/docs/resources/uuid) (resource)
- [terraform_data.ad_creation_provisioner](https://registry.terraform.io/providers/hashicorp/terraform/latest/docs/resources/data) (resource)
- [terraform_data.replacement](https://registry.terraform.io/providers/hashicorp/terraform/latest/docs/resources/data) (resource)
- [azurerm_client_config.telemetry](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/data-sources/client_config) (data source)
- [modtm_module_source.telemetry](https://registry.terraform.io/providers/azure/modtm/latest/docs/data-sources/module_source) (data source)

<!-- markdownlint-disable MD013 -->
## Required Inputs

The following input variables are required:

### <a name="input_adou_path"></a> [adou\_path](#input\_adou\_path)

Description: The Active Directory OU path.

Type: `string`

### <a name="input_dc_ip"></a> [dc\_ip](#input\_dc\_ip)

Description: The ip of the server.

Type: `string`

### <a name="input_deployment_user"></a> [deployment\_user](#input\_deployment\_user)

Description: The username for deployment user.

Type: `string`

### <a name="input_deployment_user_password"></a> [deployment\_user\_password](#input\_deployment\_user\_password)

Description: The password for deployment user.

Type: `string`

### <a name="input_domain_admin_password"></a> [domain\_admin\_password](#input\_domain\_admin\_password)

Description: The password for the domain administrator account.

Type: `string`

### <a name="input_domain_admin_user"></a> [domain\_admin\_user](#input\_domain\_admin\_user)

Description: The username for the domain administrator account.

Type: `string`

### <a name="input_domain_fqdn"></a> [domain\_fqdn](#input\_domain\_fqdn)

Description: The domain FQDN.

Type: `string`

### <a name="input_resource_group_name"></a> [resource\_group\_name](#input\_resource\_group\_name)

Description: The resource group where the resources will be deployed.

Type: `string`

## Optional Inputs

The following input variables are optional (have default values):

### <a name="input_authentication_method"></a> [authentication\_method](#input\_authentication\_method)

Description: The authentication method for Enter-PSSession.

Type: `string`

Default: `"Default"`

### <a name="input_dc_port"></a> [dc\_port](#input\_dc\_port)

Description: Domain controller winrm port in virtual host

Type: `number`

Default: `5985`

### <a name="input_destory_adou"></a> [destory\_adou](#input\_destory\_adou)

Description: whether destroy previous adou

Type: `bool`

Default: `false`

### <a name="input_enable_telemetry"></a> [enable\_telemetry](#input\_enable\_telemetry)

Description: This variable controls whether or not telemetry is enabled for the module.  
For more information see <https://aka.ms/avm/telemetryinfo>.  
If it is set to false, then no telemetry will be collected.

Type: `bool`

Default: `true`

## Outputs

The following outputs are exported:

### <a name="output_resource_id"></a> [resource\_id](#output\_resource\_id)

Description: This is the full output for the resource.

## Modules

No modules.

<!-- markdownlint-disable-next-line MD041 -->
## Data Collection

The software may collect information about you and your use of the software and send it to Microsoft. Microsoft may use this information to provide services and improve our products and services. You may turn off the telemetry as described in the repository. There are also some features in the software that may enable you and Microsoft to collect data from users of your applications. If you use these features, you must comply with applicable law, including providing appropriate notices to users of your applications together with a copy of Microsoft’s privacy statement. Our privacy statement is located at <https://go.microsoft.com/fwlink/?LinkID=824704>. You can learn more about data collection and use in the help documentation and our privacy statement. Your use of the software operates as your consent to these practices.
<!-- END_TF_DOCS -->