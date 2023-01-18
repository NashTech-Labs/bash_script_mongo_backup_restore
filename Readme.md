## Overview

The above scripts are for mongodb data backup and mongodb data backup restore. The script runs and creates a backup tar file and place it in the aws s3 bucket. Further the 

- mongo_backup.sh - This will create the backup of data of mongodb of any node where it is placed.
- mongo_restore.sh - This will restore the backup from the tar file .

#### Variables used in the script

- ENVIRONMENT - This denotes the environment where the nongo is deployed
- MONGODB_USERADMIN_PASSWORD - THe user admin password
- DCOS_MASTER_PRIVATE_IP - The private ip of dcos master node.
- AWS_S3_BUCKET - The S3 bucket name where the backup needs to be kept.
- MASTER_INSTANCE_NAME - This is the name of the instance where the dcos master is deployed.


#### How to run this script.

1 - First clone the given repo 

```
git clone < repo link > 
```

2 - Move into the scripts directory and run the script like below

```
bash mongo_backup.sh

bash mongo_restore.sh
```

**NOTE**: This script should be used on nodes of DCOS.

### 