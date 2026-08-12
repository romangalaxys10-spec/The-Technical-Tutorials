# ☁️ Ultra-Lightweight Local AWS Emulation with Floci Micro-VMs

> **Part of [The Technical Tutorials](https://github.com/romangalaxys10-spec/The-Technical-Tutorials)** collection by the Z.ai Ambassador Team.

---

## 📌 Executive Summary

**Floci** is an ultra-lightweight local AWS emulator with an astonishing **~13MB RAM footprint** and **~24ms startup time**, designed for testing AWS cloud services locally without needing an AWS account, credit card, or active API keys.

---

## 🛠️ Supported AWS Services

- **Storage & Databases**: S3, DynamoDB, RDS
- **Messaging & Compute**: SQS, SNS, Lambda
- **Security & Config**: Secrets Manager, SSM Parameter Store, KMS

---

## 🚀 Quickstart CLI

```bash
# Launch Floci local AWS emulator
floci start --port 4566

# Interact using standard AWS CLI pointing to local endpoint
aws --endpoint-url=http://localhost:4566 s3 mb s3://my-local-bucket
aws --endpoint-url=http://localhost:4566 dynamodb list-tables
```
