# ERC721-contract 
ERC721 NFT contract using only ERC721 without any library such as ERC721Enumerable and instead using our own totalSupply uint16 variable to keep track of the supply and to reduce the gas amount for minting

# ERC721 + ERC721Enumerable vs ERC721
One culprit of increased gas consumption for NFTs on Ethereum is the ERC721Enumerable library. ERC721Enumerable is a library which is widely used and adds several conveniences to NFTs and allows them to be enumerated. This ultimately makes it easier to find tokens by their associated tokenID by adding some utility functions like totalSupply, tokenByIndex, and tokenOfOwnerByIndex.

For a typical ERC721 token smart-contract, the first mint made by each wallet will cost slightly more than all future mints from the same wallet. In juxtaposition, contracts that use ERC721Enumerable see the cost increase after the first mint, only decreasing slightly for a single transaction if it’s a new wallet that is minting.

Hence, let’s look at a the same contract using only ERC721 and instead using our own totalSupply uint16 variable to keep track of the supply.
