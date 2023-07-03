// Create a variable to hold the number of NFTs.
let numberOfNFTs = 0;

// This function will take in some values as parameters, create an
// NFT object using the parameters passed to it for its metadata, 
// and store it in the numberOfNFTs variable.

function mintNFT(name, description, image) {
  // Create an NFT object with the provided metadata.

  const nft = {
    name: name,
    description: description,
    image: image
  };

  // Increment the numberOfNFTs variable.
  numberOfNFTs++;

  // Return the NFT object.
  return nft;
}

// Create a loop that will go through an array of NFTs
// and print their metadata with console.log().

function listNFTs(nfts) {
  // Iterate over each NFT in the array.
  for (let i = 0; i < nfts.length; i++) {
    const nft = nfts[i];
    // Print the metadata of the NFT.
    console.log("Name: " + nft.name);
    console.log("Description: " + nft.description);
    console.log("Image: " + nft.image);
    console.log("--------------------");
  }
}

// Print the total number of NFTs we have minted to the console.

function getTotalSupply() {
  // Return the value of numberOfNFTs.
  return numberOfNFTs;
}

// Call your functions below this line.

// Mint some NFTs and store them in the variable.
const nft1 = mintNFT("JackTheDog", "The legendary Warrior Dog", "Jack.png");
const nft2 = mintNFT("SparrowTheUndead", "A Zombie Bird", "Sparrow.png");
const nft3 = mintNFT("SilverMew", "Stealthy Cat", "SilverMew.png");

// Create an array of NFTs.
const nfts = [nft1, nft2, nft3];

// List all the NFTs.
listNFTs(nfts);

// Get the total supply of NFTs.
const totalSupply = getTotalSupply();
console.log("Total NFTs: " + totalSupply);
