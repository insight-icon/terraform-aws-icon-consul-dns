# terraform-aws-icon-consul-dns

A terraform module to create A records in AWS Route 53 to allow EC2 clients an easy endpoint to register services.
This module will query the IPs of the Consul servers in the ASG and create a RR A record with the path of:

`consul-srv.<region>.<root-domain>`

## Inputs

- zone_id: The Route 53 hosted zone ID for record insertion
- root_domain_name: The root domain of your Route 53 hosted zone
- region: The region where the instances are hosted

## Outputs

None, aside from the records being added to your zone.
