# Beatcoin

A Beginner-level cryptocurrency for educational purposes built with Typescript.

## Compile & Run

```javascript
- npm install
- npm start
```

## Usage

You can either use [Postman](https://www.postman.com/) or [curl](https://curl.haxx.se/) for creating HTTP requests to the server. I am using <b>curl</b> and here is the API of Beatcoin:

* Note that <b>Postman</b> has a pretty display of JSON data which can be easier for you to follow HTTP responses.

##### Get blockchain

```bash
curl http://localhost:3001/blocks
```

##### Mine a block

```bash
curl -X POST http://localhost:3001/mineBlock
```

##### Send transaction

```bash
curl -H "Content-type: application/json" --data '{"address": "04bfcab8722991ae774db48f934ca79cfb7dd991229153b9f732ba5334aafcd8e7266e47076996b55a14bf9913ee3145ce0cfc1372ada8ada74bd287450313534b", "amount" : 35}' http://localhost:3001/sendTransaction
```

##### Query transaction pool

```bash
curl http://localhost:3001/transactionPool
```

##### Mine transaction

```bash
curl -H "Content-type: application/json" --data '{"address": "04bfcab8722991ae774db48f934ca79cfb7dd991229153b9f732ba5334aafcd8e7266e47076996b55a14bf9913ee3145ce0cfc1372ada8ada74bd287450313534b", "amount" : 35}' http://localhost:3001/mineTransaction
```

##### Get balance

```bash
curl http://localhost:3001/balance
```

#### Query information about a specific address

```bash
curl http://localhost:3001/address/04f72a4541275aeb4344a8b049bfe2734b49fe25c08d56918f033507b96a61f9e3c330c4fcd46d0854a712dc878b9c280abe90c788c47497e06df78b25bf60ae64
```

##### Add peer

```bash
curl -H "Content-type:application/json" --data '{"peer" : "ws://localhost:6001"}' http://localhost:3001/addPeer
```

#### Query connected peers

```bash
curl http://localhost:3001/peers
```

#### References

https://lhartikk.github.io/
