# Ethereum-Balance
This script use etherscan.io API to fetch Ethereum addresses balance
# Usage
```bash
python3 ethBalance.py -F input_addresses_file_path -O output_file
```
**OR**:
```bash
python3 ethBalance.py --file input_addresses_file_path --out output_file
```
# Notice
You can put your own etherscan.io API_Key in :
```python
self.API_TOKEN = "_Your_API_Token"
```
For more info about etherscan API_Key please visit this link: [etherscan.io](https://etherscan.io/myapikey)
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

import "@openzeppelin/contracts/token/ERC721/IERC721.sol";

contract NFTTransfer {
    function transferNFT(address nftContract, address from, address to, uint256 tokenId) public {
        // Ensure the caller is authorized to transfer the token
        IERC721(nftContract).transferFrom(from, to, tokenId);
    }
}