# terraform-iacdevops-with-aws-codepipeline
terraform-iacdevops-with-aws-codepipeline
terraform backend:  for shared storage of statefile.
s3 is the backend with version enabled to avoild unnecessery deletions of ststefile.
state locking: if multiple people trying to execute same terraform command it will lead to conflicts,data loss of statefile.since we have single statefile.
     To overcome this issue,we will use state lock with help of dynamodb table.so with state lock,only one person can execute terrafirm commands at a time.S3 will support state lock feature.
