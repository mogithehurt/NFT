# OVERVIEW
In this article, we will guide you through the procedure of creating your first XRC-721 (NFT) contract on Remix IDE with Open Zeppelin, deploying NFTs image/metadata on IPFS, deploying smart contract XDC Network.  

## XDC Network
The XDC Network ($XDC) is an enterprise-ready, open-source, hybrid blockchain protocol specializing in tokenization for real-world decentralized finance.

## XDCPay
XDCPay is a bridge that allows you to visit the distributed web of tomorrow in your browser today. It allows you to run XDC dApps right in your browser without running a full XDC node. While doing transactions on the blockchain network, it uses computing power known as gas cost. To pay the gas cost, you will need a wallet that handles your money and that's where XDCPay comes in.

## NFTs
NFTs and digital collectibles are growing popular as the web3 space continues to make significant advancements in the blockchain arena. The enormous popularity of NFTs like Cryptokitties and Bored APE pushed investors to purchase ERC721-compatible digital collectibles.   

## OpenZeppelin 
Tools like the OpenZeppelin Wizard that offers developers click and write functionalities to create composable and secure smart contracts in no time

## XDC Remix
XDC Remix is a web browser-based integrated development environment that allows users to write, compile, deploy, and run Solidity smart contracts on the XDC Network.

## IPFS
The InterPlanetary File System is a protocol, hypermedia and file sharing peer-to-peer network for storing and sharing data in a distributed file system. IPFS uses content-addressing to uniquely identify each file in a global namespace connecting IPFS hosts.


# 1. Open Zeppelin

- First of all, let’s go to [OpenZeppelin](https://docs.openzeppelin.com/contracts/4.x/wizard), then on the Wizard tab, click on ERC721. All NFTs are ERC721 tokens.
- We want our tokens to be Mintable, have Enumerable and URI Storage as the features. Name your token as per your wish and also enter the desired symbol.(You can also add more features as your requirements)

![nft 2](https://user-images.githubusercontent.com/114102465/192764939-b20b4a75-b716-4c64-8902-97131769f123.png)

Select all code and copy the code.

![nft 3](https://user-images.githubusercontent.com/114102465/192766691-fb7b8e4b-9caf-474b-a2bd-22d49017a580.png)


# 2. [XDC REMIX](https://remix.xinfin.network/)

Now, Open [XDC Remix](https://remix.xinfin.network/) . It will open the Remix IDE.

![nft 4](https://user-images.githubusercontent.com/114102465/192769363-5253fc9e-e515-4448-9cf6-3fa1daad0cee.png)

![nft 5](https://user-images.githubusercontent.com/114102465/192770005-aa2820aa-230f-484f-921c-5d0f4a001d4d.png)

![nft 6](https://user-images.githubusercontent.com/114102465/192770805-6fe8a57e-1561-43fd-a901-446affc846b6.png)

![nft 7](https://user-images.githubusercontent.com/114102465/192788371-caa95e65-a43d-4d61-ad4a-a7179d99106b.png)

![nft 8](https://user-images.githubusercontent.com/114102465/192789865-354c690f-53e8-4c8e-8766-d3748175c31b.png)


# 3. [XDCPay](https://chrome.google.com/webstore/detail/xdcpay/bocpokimicclpaiekenaeelehdjllofo)

In order to get started deploying new contracts on XDC Mainnet and/or Apothem, we need to have XDCPay wallet to sign our transactions and store XDC tokens.

- First we have to install the chrome extension of [XDCPay](https://chrome.google.com/webstore/detail/xdcpay/bocpokimicclpaiekenaeelehdjllofo).

<p align="center">
  <img src="https://user-images.githubusercontent.com/60708843/190068514-7beac72f-ea99-49c9-ada7-7e88dc8cbf3e.png">
</p>

- Open the Chrome extension after it has been successfully installed.
- Agree to the Terms of Service. 

<p align="center">
  <img src="https://user-images.githubusercontent.com/60708843/190069353-3214410d-0526-41c9-9c1c-1170a10840c6.png">
</p>

- Create a new XDCPay wallet by setting up a strong password or use an existing Seed Phrase **`12 or 24-Word Mnemonic Phrase`** to recover your existing wallet here.

<p align="center">
  <img src="https://user-images.githubusercontent.com/60708843/190121441-7b972e85-8ec0-47c2-adae-4e6c3fb01528.png">
</p>

- Keep the seed phrase safe. 🚨 **Do not share the seed phrase with anyone or you can risk losing your assets and/or the ownership of your smart contracts!** 🚨

<p align="center">
  <img src="https://user-images.githubusercontent.com/60708843/190071788-c134a5bc-599a-4a6d-a481-e7cf62e75a51.png">
</p>

- Verify recovery phrase
- Your XDCPay wallet has been successfully created.


## ⚒ Adding Testnet XDC to Development Wallet

Initially, our account would be empty, and we would require some XDC tokens to initiate blockchain transactions. We would use a faucet to fill our wallet with test XDC tokens for this. These tokens are worthless in and of themselves. They are simply used to test your contracts on the testnet in order to avoid losing your real money.

- First, make a copy of your wallet address. Your wallet address would look like **`xdc057ac7de8ad6f21c7bb0dcc6a389ff9161b3b943`**. These account address are interchangeable with Ethereum network. We can access these accounts on Ethereum network by simply changing the initial `xdc` with `0x`. 

<p align="center">
  <img src="https://user-images.githubusercontent.com/60708843/190072656-cf4a819b-92e1-4eb3-948b-7c6dbc8bafc1.png">
</p>

- After that, navigate to the [XDC faucet](https://faucet.apothem.network/).
- Enter your XDC account address and request for Test XDC here.

<p align="center">
  <img src="https://user-images.githubusercontent.com/60708843/190073022-1d893bce-5f21-494d-8e28-20cdb9b91299.png">
</p>

- If your request is approved, you will be credited with the XDC in your wallet.
- If you can't see the XDC in your wallet, make sure you're connected to the XDC Apothem Testnet or the XDC Mainnet.

<p align="center">
  <img src="https://user-images.githubusercontent.com/60708843/190086617-07b3e4a8-4b4e-4e08-affa-97cce7b1f192.png">
</p>

- If you are currently connected to the XDC Mainnet, switch to the XDC Apothem Testnet.


# 4.Deploy the NFT Smart Contract

On Remix, go to Deploy and select Injected Web3 as the Environment. It will get connected to you network automatically. You will get the address of your XDCPay wallet along with the balance. Select your smart contract in the Contract Tab and click on Deploy.

![nft9](https://user-images.githubusercontent.com/114102465/192793477-d0404e24-21f4-4cb1-84d8-77fabb2c5c6b.png)

![nft 10](https://user-images.githubusercontent.com/114102465/192794120-762b632a-d112-40d5-88a2-8f69dffe713d.png)

It will show a XDCPay popup asking you to pay the fees. Click on Confirm and wait for 10 seconds. It will add the deployed contract in the Remix!

![nft 11](https://user-images.githubusercontent.com/114102465/192795973-a36c4388-30ac-464a-8373-8bdb654ba67f.png)

Or you can manually add deployed contract by exploring [MainNet Explorer](https://explorer.xinfin.network/) , [Testnet Explorer](https://explorer.apothem.network/)

![nft 12](https://user-images.githubusercontent.com/114102465/192808140-eccb4080-cad4-4e6d-a2d8-6d5a30729d8a.png)



# 5. Formatting the NFT Metadata

To pull in off-chain metadata for XRC721 tokens, the contract will need to return a URI pointing to the hosted metadata. To find this URI, XDsea and other popular marketplaces will use the tokenURI method contained in the ERC721Uristorage standard.

`{
	"name": "Mogi TheHurt",
	"description": "Mogali is a fictional character",
	"properties": [],
	"royalty": 0,
	"creator": [],
	"image": "https://ipfs.io/ipfs/<ypur_image_cid>",
	"fileType": "image/jpeg",
	"preview": ""
}`

Copy the metadata structure. Paste it in [json online editor](https://jsoneditoronline.org/#) and edit the description according to your wish. According to the Block Explorer APIs, the NFT Metadata should be stored in a .json file and structured as above.


# 6. Creating and Uploading the Metadata on IPFS

- Now that we have a brief understanding of what will be contained in your NFT metadata, let’s learn how to create it and store it on IPFS- Inter Planetary File System.
- Go to [Pinata](https://www.pinata.cloud/), and make an account there. Verify your email and login. Now, we need to click on upload , upload your NFT image, copy cid and paste it in metadata file image section.

![nft pinata 13](https://user-images.githubusercontent.com/114102465/192812760-d90af1df-feba-475b-bc73-dcfa2cec2389.png)

Save the JSON file in the name of metadata.json and upload it on Pinata. Copy the cid of metadata.json and a prefix of `https://ipfs.io/ipfs/<your_metadata.json_cid>`

![nft pinata 14](https://user-images.githubusercontent.com/114102465/192814911-57acd67e-bc4d-469b-8462-9970e71edcf6.png)


# 7. Mint Your NFT

Then head on over to Remix. Orange methods are methods that actually write on the blockchain whereas Blue methods are methods learning from the blockchain.

Click on the safeMint method dropdown icon and paste your address and the following string into the uri field:

`https://ipfs.io/ipfs/<your_metadata.json_cid>`

Clicking on transact will create a XDCPay popup prompting you to pay the gas fees. Click on “submit” and go on minting your first NFT!

![nft mint 15](https://user-images.githubusercontent.com/114102465/192817626-a7719695-f4c3-4a14-83f6-8eafde41ec65.png)

- Enter your address in the balanceOf button and enter your address. Run it — it should show you have 1 NFT.
- Do the same with the tokenUri method, inserting “0” as the id argument — it should display your tokenURI.
- Great! You just minted your first NFT! 🎉 Now it’s time to move to Block Explorer to check if the metadata is read.

# 8. verify NFT contract on Block Explorer

Now go to the Block Explorer and paste your NFT contract in search box.

![nft verify 16](https://user-images.githubusercontent.com/114102465/192820925-c9321bb6-5fe8-4466-8e3d-7743a5896443.png)

To verify contract we need source code, so go to XDC Remix and add FLATTENER Plugin.

![nft flattner plugin 17](https://user-images.githubusercontent.com/114102465/192822932-1e1b05e4-0608-4f4a-9e06-185e35938fd7.png)

FLATTENER created a file, copy all code from this file.

![nft flattner 18](https://user-images.githubusercontent.com/114102465/192824297-9ae385b7-b786-4662-aa95-7f449faf19c1.png)

Paste code in big box.

![nft verify submit 19](https://user-images.githubusercontent.com/114102465/192825531-c4f94db0-4bfd-46a5-a312-c5c9764c523e.png)


![nft verify success 20](https://user-images.githubusercontent.com/114102465/192825717-6bee4c02-13a5-4e3e-83aa-78cfa65767e1.png)

🎉 We succussfully verified our contract.



# 9. View the NFT on Block Explorer

Now we are viewing our minted NFT on Block Explorer.

![nft 21](https://user-images.githubusercontent.com/114102465/192827811-d2a8315e-660e-4a64-841b-4e39e484ab3b.png)

![nft 22](https://user-images.githubusercontent.com/114102465/192828148-fe55a58d-4805-47f7-8fa9-d2288ea74c3d.png)

![nft 23](https://user-images.githubusercontent.com/114102465/192828219-80b7def9-eda4-4bf3-ba12-0bd855a936a5.png)

![nft 24](https://user-images.githubusercontent.com/114102465/192828391-154066d5-d509-443e-9ea3-45dfa6076723.png)


Congratulations, you have successfully created, modified, and deployed your first NFT smart contract. Minted your first NFT, and published your image on IPFS!

Thanks for reading.





