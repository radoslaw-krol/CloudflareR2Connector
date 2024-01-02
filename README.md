## Cloudflare R2 Connector

This notebook outlines the process of connecting to Cloudflare's R2 storage service. It includes steps for authentication, managing storage buckets, and performing file operations such as uploading, downloading, and deleting files. Code cells demonstrate API calls and handle responses for various tasks, ensuring seamless interaction with the R2 service.

You need to have a access key and access id - read this on how to set it up: https://developers.cloudflare.com/r2/api/s3/tokens/

From my experience keep default names of keys in .env otherwise you might experience a bug where boto3 cant establish connection even if provided keys are correct.

access_key_id

access_key_secret

More on boto3 in CF R2 and default names here: https://developers.cloudflare.com/r2/examples/aws/boto3/

For url, if you have specified jurisdiction (region) while creating R2 bucket, you have to access it using jurisdiction specific endpoint. For example:

European Union (EU): https://<ACCOUNT_ID>.eu.r2.cloudflarestorage.com

FedRAMP: https://<ACCOUNT_ID>.fedramp.r2.cloudflarestorage.com