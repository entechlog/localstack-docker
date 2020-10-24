# localstack-docker

## demo-localstack-redshift

- Documentation
	- https://github.com/localstack/localstack
	- https://docs.aws.amazon.com/redshift/latest/mgmt/getting-started-cli.html

- Start localstack by running `docker-compose up`

- Verify the status of service by running `curl http://localhost:4566/`

- Create redshift cluster by running
```
aws redshift create-cluster --cluster-identifier entechlog-redshift-cluster-01 --master-username masteruser --master-user-password TopSecret1 --node-type ds2.xlarge --cluster-type single-node --endpoint http://localhost:4566
```
- Describe redshift cluster by running
```
aws redshift describe-clusters --endpoint http://localhost:4566
```