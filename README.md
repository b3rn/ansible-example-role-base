# ansible-example-role-base
> A very simple role that handles base configuration across various Unix/Linux families.

## Role Variables
### RHN Subscription ([docs](http://docs.ansible.com/ansible/redhat_subscription_module.html))
*Note: use either `rhn_org_id` + `rhn_activationkey` or `rhn_username` + `rhn_password`*
- `**rhn_rhsm_base_url**`: (optional) CDN baseurl
- `**rhn_server_hostname**`: (optional) Red Hat Network server
- `**rhn_server_insecure**`: (optional) enable or disable https server certificate verification when connecting to `rhn_server_hostname`
- `**rhn_autosubscribe**`: (optional) upon successful registration, auto-consume available subscriptions
- `**rhn_username**`: (required with password) Red Hat Network username
- `**rhn_password**`: (required with username) Red Hat Network password
- `**rhn_org_id**`: (required with activationkey) organization ID to use in conjunction with `rhn_activationkey`
- `**rhn_activationkey**`: (required with org_id) activation key for use with registration
- `**rhn_pool_regex**`: (optional) specify a subscription pool name to consume
- `**enable_epel**`: (optional) whether or not to enable EPEL
- `**enable_optional**`: (optional) whether or not to enable the RHEL optional repo

### Packaging
- `**common_base_packages**`: (optional) a list of packages to install on all machines
- `**debian_base_packages**`: (optional) a list of packages to install on all Debian machines
- `**rhel_base_packages**`: (optional) a list of packages to install on all RHEL machines
- `**freebsd_base_packages**`: (optional) a list of packages to install on all FreeBSD machines
