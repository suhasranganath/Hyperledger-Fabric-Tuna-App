# Hyperledger Fabric Tuna App
This application demonstrates the creation and transfer of tuna fish shipments between actors leveraging Hyperledger Fabric in the supply chain. 

This application is part of LinuxFoundationX course that I took to learn about HyperLedger. 
[Certificate(click to view!)](http://bit.ly/LFS171xCeritificate)

## Setup
<ol>
  <li> Make sure you are in <b>tuna-app</b> folder</li>
  <li> Start the Hyperledger Fabric network with the following command: </li>
  <pre><code>$ ./startFabric.sh</code></pre>
  <li> Install the required libraries from the package.json file </li>
  <pre><code>$ npm install</code></pre>
  <li> Register the Admin and User components of our network</li>
  <pre><code>$ node registerAdmin.js
$ node registerUser.js</code></pre>
  <li> Start the client application </li>
  <pre><code>$ node server.js</code></pre>
</ol>

The network will be setup on port <b>8000</b>. You can access it through <b>localhost:8000</b>

## Troubleshoot
To resolve persmission issues while running <b>./startFabric.sh</b>
<pre><code>$ chmod a+x startFabric.sh</code></pre>

If you get error while creating user/admin components. Try following commands
<pre><code>$ rm -rf ~/.hfc-key-store
$ node registerAdmin.js
$ node registerUser.js</pre></code>

## Shutdown the network and clean up images

Following commands remove all Docker containers and images created.
<pre><code> $docker rm -f $(docker ps -aq) 
 $docker rmi -f $(docker images -a -q) </pre></code>


This code is based on code written by the Hyperledger Fabric community. Source code can be found here: (https://github.com/hyperledger/fabric-samples).

Please do sign up for the course on edX.
[Course Link](https://www.edx.org/course/blockchain-business-introduction-linuxfoundationx-lfs171x)
