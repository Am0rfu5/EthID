# Digital Identity Model

This **Decentralized Application (DApp)** is a development model based on the **Self-Sovereign Identity** concept.

This project seeks to decentralize **Digital Identity** and remove the fragmentation caused by creating a different identity for each service. The application doesn't store user information directly but does encrypts and send it to the Ethereum blockchain, making it possible that can be read by a Service Provider.

While Ethereum exists, your Identity exists.

## Setup

Go to the repository folder.
```bash
$ npm install //This take a while with some update recommendations.
$ truffle install oraclize-api
``` 

Start Ganache or Ganache-cli

```bash
$ mkdir ethereum-bridge
$ git clone https://github.com/oraclize/ethereum-bridge ethereum-bridge
$ cd ethereum-bridge
$ npm install
$ node bridge -a 9 // This get the 9 account of Ganache
```

From the output of: `node bridge -a 9` copy the line that looks like:

`OAR = OraclizeAddrResolverI(0x6f485C8BF6fc43...)`

Ethereum bridge try to connect to http://localhost:8545

**Replace the existing `OAR = OraclizeAddrResolverI(0x6f485C8BF6fc43eA21...)` with the one you wrote down before**

Open a new terminal and in the path of the project.

```bash
$ truffle migrate --reset // Use --reset if you have a previous build.
```

Be sure that the account (usually the first account of Ganache) has at least 15 ethers (used for Oraclize).

If the migration is successful.

```bash
$ npm run dev

```
Go to [http//localhost:8080](http://localhost:8081/) (if port 8080 is in use, try 8081).

```

Project is running at http://localhost:8081/

```

```bash
$ node bridge -a 9 -H 127.0.0.1 -p ganachePort --dev
```

for example:

```bash
$ node bridge -a 9 -H 127.0.0.1 -p 9545 --dev 
```