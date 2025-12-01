# MinIO – Installation & Configuration
MinIO is a high-performance, S3‑compatible object storage server.

**Installation**
1. Download the server binary:

bash
```
wget https://dl.min.io/server/minio/release/linux-amd64/minio
chmod +x minio
```
2. Start the service:

bash
```
./minio server /data
```
**Configuration**
- Access the console at:

text
```
http://<server>:9000
```
- Configure:

  - Access and secret keys

  - Buckets

  - IAM-style policies

  - TLS certificates and HTTPS
