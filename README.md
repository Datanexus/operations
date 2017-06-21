# operations
operational tasks

## kafka
This configures each broker in the kafka cluster as a client for initial testing.

    AWS_PROFILE=datanexus ./add-client -e "ansible_user=centos key_path=$tenant/keys cloud=aws ec2_region=us-east-1 tenant=datanexus project=demo domain=development application=kafka tenant_config_path=$tenant"