## adding a replica
For standalone instance:

    AWS_PROFILE=datanexus ./add-replica -e "cloud=aws ec2_region=ap-southeast-2 domain=development project=demo tenant=datanexus key_path=$tenant/keys"
    
For an existing master/replica pair:

    AWS_PROFILE=datanexus ./add-replica -e "cloud=aws ec2_region=ap-southeast-2 domain=development project=demo tenant=datanexus key_path=$tenant/keys cluster=a"