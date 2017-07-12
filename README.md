# operations
operational tasks

## kafka
This configures each broker in the kafka cluster as a client for initial testing.

    AWS_PROFILE=datanexus ./add-client -e "ansible_user=centos key_path=$tenant/keys cloud=aws ec2_region=us-east-1 tenant=datanexus project=demo domain=development application=kafka tenant_config_path=$tenant"
    
### postgresql
Read the tenant config/site.yml file and create/delete listed users and databases

    AWS_PROFILE=datanexus ./users -e "ansible_user=centos key_path=$tenant/keys cloud=aws ec2_region=us-east-1 tenant=datanexus project=demo domain=production application=postgresql cluster=a tenant_config_path=$tenant"

#### Testing
Network encryption is mandatory, so on the master server you connect via the linux socket without needing to specify a host:

    sudo -i -u postgres psql -U ADDED_USER ADDED_DB