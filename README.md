# tinybird_demo
This is a demo for Tinybird.

This demo includes:

## Datasources
Real UK Police crime data (puplic dataset)
- reported street criime
- reported street crime outcomes

Tinybird Pipes
- police outcomes clean
- police street crime crlean
- crime summary
- outcome summary
- closed crime outcomes

# Getting started
Requirements
The following python packages are required:

tinybird-cli

#Installation


Setup
AWS (Optiona)
S3
First, create an S3 bucket to use for the demo (or you can reuse an existing bucket).

This demo will create a prefix of tinybird/fake in this bucket.

IAM
Next, create or find an IAM User that has appropriate permissions to Get & Put in your S3 bucket.

Finally, create an access key for this IAM User.

Keep the Access Key and Secret Key handy for the next step.

env vars
The following env vars are used for the demo. You can export these as normal, or create a dotenv file data_gen/.env and they will be loaded at runtime.

METHOD = 'kafka' # Must be 'kafka' or 's3'
EVENT_COUNT = 100 # Must be a valid, positive integer

# Only required if 's3' is set as METHOD
SECRET_KEY = '' # Your AWS IAM Secret Key
ACCESS_KEY = '' # Your AWS IAM Access Key
REGION = '' # Your AWS Region
S3_BUCKET = '' # Your AWS S3 bucket name

# Only required if 'kafka' is set as METHOD
KAFKA_TOPIC = '' # Your Kafka topic name
KAFKA_BROKERS = '' # Your broker list with port e.g. my-broker:9092
KAFKA_SECURITY_PROTOCOL = '' # Must be SASL_SSL, SASL_PLAINTEXT or PLAINTEXT, defaults to PLAINTEXT
KAFKA_SASL_MECHANISM = '' # Must be PLAIN
KAFKA_USER = '' # Kafka User
KAFKA_PASSWORD = '' # Kafka Password
Running
Start by generating the fake data.

Run

python data_gen/data_gen.py
