# Apache Superset – Installation & Configuration (On Premise)
Apache Superset is an open-source BI and data visualization platform.
**Prerequisites**
- Linux server (Ubuntu 22.04 recommended)
- Python 3.9+
- MariaDB or PostgreSQL for metadata
- Redis for caching
**Installation**
1. Install OS dependencies:
bash
```
sudo apt update
sudo apt install -y build-essential libssl-dev libffi-dev python3-venv python3-dev redis-server
```
2. Create and activate a virtual environment:
bash
```
python3 -m venv venv
source venv/bin/activate
```
3. Install Superset:
bash
```
pip install apache-superset
```
**Configuration**
1. Initialize the metadata database:
bash
```
superset db upgrade
```
2. Create an admin user:
bash
```
superset fab create-admin
```
3. Initialize roles, permissions, and default assets:
bash
```
superset init
```
4. Start the service:
bash
```
superset run -p 8088 --with-threads
```
Access the UI at:
text
```http://<superset-host>:8088```
