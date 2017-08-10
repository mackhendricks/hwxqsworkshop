# Lab 4a: Install HDF (Nifi Only)

Assumptions:

- HDF (Nifi Only) has been downloaded and placed in the /tmp directory of your management node

1. Login to your assigned management node
2. Execute
```cd /usr/local/share
sudo tar -xzvf /tmp/nifi-*
cd ./nifi*
sudo ./bin/nifi.sh install
sudo sed -i s/8080/80/ conf/nifi.properties
```

Question:

- What does the sed command do in the above statement and why is it needed?

# Lab 4b: Start Using HDF

1. sudo ./bin/nifi.sh start
2. In your web browser go to http://[managementnode ip]:9090/nifi

Question:

- Where's the logs for HDF?

Resources:

HDF Deployment Scenarios:

https://docs.hortonworks.com/HDPDocuments/HDF3/HDF-3.0.0/bk_planning-your-deployment/content/ch_deployment-scenarios.html
