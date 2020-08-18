## Restrict API calls S3 from specific IP addresses
- IAM role only list,get,put object to spesific bucket
- AWS Key only can use in AWS Subnet or GCP Cloudnat or Office IP Public
- Example IP Cloud NAT GCP = 11.11.11.11/32
- Example IP NAT Gatewat or Subnet VPC AWS = 22.22.22.22/32


## Test use key aws s3 we create only can use in network AWS and GCP
- Test Copy file from outside IP Public (telkom etc)
```
aws s3 cp lol.jpeg s3://zeus-cloud/lol.jpeg
upload failed: ./lol.jpeg to s3://zeus-cloud/lol.jpeg An error occurred (AccessDenied) when calling the PutObject operation: Access Denied
```

- Test list object from outside IP Public (telkom etc)
```
aws s3 ls s3://zeus-cloud
An error occurred (AccessDenied) when calling the ListObjectsV2 operation: Access Denied
```
