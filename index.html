import hashlib
import json
import time

class DigiCoin:
    def __init__(self):
        self.chain = []
        self.balances = {
            "Alice": 100,
            "Bob": 100,
            "Charlie": 100
        }
        self.pending_transactions = []
        self.create_block(0, "Genesis Block")

    def create_block(self, proof, previous_hash):
        block = {
            "index": len(self.chain) + 1,
            "timestamp": time.time(),
            "transactions": self.pending_transactions.copy(),
            "proof": proof,
            "previous_hash": previous_hash
        }

        self.pending_transactions = []
        self.chain.append(block)
        return block

    def get_hash(self, block):
        encoded = json.dumps(
            block, sort_keys=True
        ).encode()
        return hashlib.sha256(encoded).hexdigest()

    def transfer(self, sender, receiver, amount):
        if sender not in self.balances:
            print("Sender wallet not found!")
            return

        if receiver not in self.balances:
            self.balances[receiver] = 0

        if amount <= 0:
            print("Invalid amount!")
            return

        if self.balances[sender] < amount:
            print("Insufficient balance!")
            return

        self.balances[sender] -= amount
        self.balances[receiver] += amount

        transaction = {
            "sender": sender,
            "receiver": receiver,
            "amount": amount
        }

        self.pending_transactions.append(transaction)
        print("Transaction successful!")

    def mine_block(self, miner):
        reward = 10
        self.balances[miner] = self.balances.get(miner, 0) + reward

        previous_hash = self.get_hash(self.chain[-1])
        block = self.create_block(1, previous_hash)

        print("\nBlock mined successfully!")
        print("Mining Reward:", reward, "DigiCoins")
        print("Block Number:", block["index"])

    def show_balance(self):
        print("\n--- DigiCoin Wallet Balances ---")
        for user, balance in self.balances.items():
            print(user, ":", balance, "DGC")

    def show_blockchain(self):
        print("\n--- DigiCoin Blockchain ---")
        for block in self.chain:
            print(json.dumps(block, indent=4))


coin = DigiCoin()

while True:
    print("\n===== DIGICOIN SYSTEM =====")
    print("1. Show Wallet Balances")
    print("2. Transfer DigiCoins")
    print("3. Mine DigiCoins")
    print("4. View Blockchain")
    print("5. Exit")

    choice = input("Enter your choice: ")

    if choice == "1":
        coin.show_balance()

    elif choice == "2":
        sender = input("Enter sender name: ")
        receiver = input("Enter receiver name: ")
        amount = float(input("Enter amount: "))
        coin.transfer(sender, receiver, amount)

    elif choice == "3":
        miner = input("Enter miner name: ")
        coin.mine_block(miner)

    elif choice == "4":
        coin.show_blockchain()

    elif choice == "5":
        print("Thank you for using DigiCoin!")
        break

    else:
        print("Invalid choice! Try again.")
