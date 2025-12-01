# MongoDB – Installation & Configuration
MongoDB is a document database.

**Installation (Ubuntu)**
bash
```
sudo apt update
sudo apt install -y mongodb-org
sudo systemctl enable --now mongod
```
**Configuration**
1. Edit /etc/mongod.conf for bind address:

text
```
net:
  bindIp: 0.0.0.0
```
(Only if remote access is required; otherwise keep it bound to localhost.)

2. Create users and roles using the mongo shell or mongosh.

3. Enable and configure a replica set:

js
```
rs.initiate({
  _id: "rs0",
  members: [
    { _id: 0, host: "mongo1:27017" },
    { _id: 1, host: "mongo2:27017" },
    { _id: 2, host: "mongo3:27017" }
  ]
})
```
