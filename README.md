There are 2 cloudformation scripts: network.yml and servers.yml.

To setup the application, just run the following commands:

```
aws cloudformation create-stack --stack-name project2-network --template-body file://network.yml --parameters file://network-params.yml
aws cloudformation create-stack --stack-name project2-servers --template-body file://servers.yml --parameters file://server-params.yml
```

Notice that you will need to wait for the network stack to finish creating to be able to create the server stack because there are some dependent variables.

Several resources on the script are based upon the scripts developed during the classes and written by Carlos Rivas.
