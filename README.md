# go_blockchain
This is a simple blockchain implementation in Go.

## Features

| Feature                                | Description                                      |
| -------------------------------------- | ------------------------------------------------ |
| Block creation and validation          | Implements the creation and validation of blocks |
| Proof-of-work consensus algorithm      | Implements the proof-of-work consensus algorithm |
| Transaction management                 | Handles transactions within the blockchain       |
| Chain integrity and validation         | Ensures the integrity and validity of the chain  |

## Getting Started

### Prerequisites
- Go 1.15 or above

### Installation
1. Clone the repository:
```shell
git clone https://github.com/Avionic22/go_blockchain.git
```

2. Run the wallet server
```shell 
cd go_blockchain/wallet_server
go build
./wallet_server
```
3. Run the blockchain node:
```shell
cd go_blockchain/blockchain_server
go build
./blockchain_server
```

## Usage

- To view the wallet balance:
```shell
curl -d "blockchain_address=0x000000" http://localhost:8080/wallet/amount
```

- To create a new transaction:
```shell
curl -X POST -H "Content-Type: application/json" -d '{"sender_private_key": "private_key", "sender_blockchain_address": "0x0000", "recipient_blockchain_address": "0x0001", "sender_public_key": "public_key", "value": 20.00}' http://localhost:8080/transaction
```

- To view the current blockchain:
```shell
curl http://localhost:5000/
```

- To start mining:
```shell
curl http://localhost:5000/mine/start
```



