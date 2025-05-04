# Full-Web-Application-Deployment-on-AWS


##**1. Database setup**

- Installing dataset from Kaggle https://www.kaggle.com/datasets

- Launching database in RDS and connecting it with Debeaver

- Creating table named tbl_<your_first_name>_<dataset_name>

- Importing CSV file to the database in Debeaver

  
##**2. S3 Static Hosting**

- Create an S3 bucket for static website hosting

- Uploading HTML and file should be named: index_<your_first_name>.html

- Set up the correct S3 bucket policy to make it public

### 📁 S3 Bucket Policy

The following policy allows public access to the S3 bucket and its contents:

```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:ListBucket",
            "Resource": "arn:aws:s3:::xusanboy-static-site"
        },
        {
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:*",
            "Resource": "arn:aws:s3:::xusanboy-static-site/*"
        }
    ]
}

```bash
# Pull the latest PostgreSQL Docker image
docker pull postgres:latest

# Create a Docker container for the PostgreSQL database
docker run --name muhammad-db -e POSTGRES_USER=Muhammad -e POSTGRES_PASSWORD=1234 -d -p 5432:5432 postgres:latest


# Verify the container is running
docker ps

# Access the running PostgreSQL container
docker exec -it muhammad-db psql -U Muhammad
```
