# Decentralized-Blockchain
Basic implementation of a decentralized blockchain with multiple nodes.
class BlockchainNode:
    def __init__(self, blockchain):
        self.blockchain = blockchain

    def receive_new_block(self, new_block):
        # Validate the new block and append it to the blockchain if valid
        if validate_block(new_block, self.blockchain[-1]):
            self.blockchain.append(new_block)

# Example usage
node_A = BlockchainNode(blockchain)
node_B = BlockchainNode(blockchain)

# Assume node_A and node_B are part of a decentralized network
# When node_A mines a new block, it broadcasts it to the network
new_block = mine_block()
node_B.receive_new_block(new_block)
