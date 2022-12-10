# click through AWS console to create EFS
login to AWS console and search for service _EFS_   
click through wizard , use our course VPC and all 3 AZs
*specify the security group of your EC2-worker-nodes, to be applied to EFS as well*

# add amazon-efs-utils
install the package *amazon-efs-utils* on all worker nodes


```
ssh -i <<eks-course.pem>> ec2-user@<<ec2-workernode>> "sudo yum install -y amazon-efs-utils"

```
```
steps:
- Cluster creation
- node instance - add amazon-efs-utils
- efs provision - security group with source (clustersharednodegroup) - NFS
- efs mount points - subnets and efs-sg
- instance IAM role access for EFSFullAccess
- create rbac
- create efs prov
- create storage
- wp and sql 