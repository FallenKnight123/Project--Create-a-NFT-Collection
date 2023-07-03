// create a variable to hold your NFT's
let numberOfNFTs = 0;

function mintNFT(name, description, image) {
  let nft = {
    name: name, 
    description: description,
    image: image
  };
  numberOfNFTs++;
  return nft;
}

function listNFTs() {
  // Assuming you have an array of NFT objects
  // Replace this array with your actual array of NFT objects
  let nfts = [
    {
      name: "NFT 1",
      description: "This is NFT 1",
      image: "nft1.png"
    },
    {
      name: "NFT 2",
      description: "This is NFT 2",
      image: "nft2.png"
    }
  ];

  for (let i = 0; i < nfts.length; i++) {
    console.log("Name: " + nfts[i].name);
    console.log("Description: " + nfts[i].description);
    console.log("Image: " + nfts[i].image);
  }
}

function getTotalSupply() {
  return numberOfNFTs;
}

// Call your functions below this line

// Mint a new NFT and store it in the variable
let newNFT = mintNFT("My NFT", "This is my first NFT", "nft.png");

// List all NFTs' metadata
listNFTs();

// Print the total number of NFTs
console.log("Total Supply: " + getTotalSupply());
