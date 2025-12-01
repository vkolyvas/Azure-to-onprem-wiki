# ELK Stack (Elasticsearch, Logstash, Kibana)
The ELK stack provides search, log ingestion, and visualization.

**Installation**
1. Add the official Elastic repository.

2. Install Elasticsearch:

bash
```
sudo apt install -y elasticsearch
```
3. Install Logstash:

bash
```
sudo apt install -y logstash
```
4. Install Kibana:

bash
```
sudo apt install -y kibana
```
Enable and start services as needed.

**Configuration**
- Elasticsearch:

  - Configure cluster name, node roles, and JVM heap.

  - Secure with TLS and user authentication.

- Logstash:

  - Define pipelines in ```/etc/logstash/conf.d/*.conf```.

  - Set inputs (Beats, syslog, Kafka), filters (grok, json), and outputs (Elasticsearch).

- Kibana:

  - Point to Elasticsearch URL.

  - Configure role-based access control.

  - Create index patterns, dashboards, and visualizations.

- Beats / Agents:

  - Configure Filebeat, Metricbeat, or other shippers to send data to Logstash or Elasticsearch.
