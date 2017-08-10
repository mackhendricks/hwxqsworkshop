# Lab 4: Install HDF (Nifi Only)

Assumptions:

- HDF (Nifi Only) has been downloaded and placed in the /tmp directory of your management node

1. Login to your assigned management node
2. cd /usr/local
3. Execute
```
sudo tar -xgvf /tmp/nifi-*
```
4. cd ./nifi*
5. sudo ./nifi.sh install
6. sudo ./nifi.sh start
7. In your web browser go to http://[managementnode]:9090/nifi

