# python-send-heartbeat

```bash
export AWS_VAULT_FILE_PASSPHRASE="$(cat /root/.awsvaultk)"
```

```bash
aws-vault exec dev -- terraform -chdir=./terraform/01 init
```

```bash
aws-vault exec dev -- terraform -chdir=./terraform/01 apply --auto-approve
```

```bash
source ./terraform/01/terraform.tmp
```

```bash
export HEARTBEAT_QUEUE_URL=<https://sqs>.<REGION>.amazonaws.com/<ACCOUNT_ID>/<SQS_NAME>
```

```bash
python ./send_heartbeat/lambda_function.py
```

```bash
export HEARTBEAT_RUN_ONCE=true
```

```bash
python ./send_heartbeat/lambda_function.py
```

```bash
mkdir -p ./terraform/02/external
```

```bash
zip -r -j ./terraform/02/external/send_heartbeat.zip ./send_heartbeat
```

```bash
aws-vault exec dev -- terraform -chdir=./terraform/02 init
```

```bash
aws-vault exec dev -- terraform -chdir=./terraform/02 apply --auto-approve
```
