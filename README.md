# Blockchain Research

## 
__Fabric - example blockchain platform__
* Fabric samples Located at [/fabric/examples/fabric-samples](https://github.com/odu-vmasc/Blockchain/tree/master/fabric/examples/fabric-samples).

   Both examples utilize a crypto-config.yaml file that controls the crypto settings and have scripts to start the network.

   The scripts utilize the cryptogen executable located [/fabric/build/bin/](https://github.com/odu-vmasc/Blockchain/tree/master/fabric/build/bin)
   * [First-network](https://github.com/odu-vmasc/Blockchain/tree/master/fabric/examples/fabric-samples/first-network) just uses crypto cert files without certificate authority
   Can run the build your first network (byfn.sh) script file to automatically generate files and run network.
   To modify the number of peer nodes and scale the network modify the docker-compose file that is being used (docker-compose-cli by default)
   * [Basic-network](https://github.com/odu-vmasc/Blockchain/tree/master/fabric/examples/fabric-samples/basic-network) uses a certificate authority
   Can run the start.sh script file to start up the network

