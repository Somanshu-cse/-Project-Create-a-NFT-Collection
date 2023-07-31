# -Project-Create-a-NFT-Collection



// Assessment Requirements
// 1. Create a variable that can hold a number of NFT's. What type of variable might this be?
// 2. Create an object inside your mintNFT function that will hold the metadata for your NFTs. 
//    The metadata values will be passed to the function as parameters. When the NFT is ready, 
//    you will store it in the variable you created in step 1
// 3. Your listNFTs() function will print all of your NFTs metadata to the console (i.e. console.log("Name: " + someNFT.name))
// 4. For good measure, getTotalSupply() should return the number of NFT's you have created


const nftsCollection = [];

function mintNFT(name, hairColor, shirtType, accessory) {
  const nft = {
    name: name,
    hairColor: hairColor,
    shirtType: shirtType,
    accessory: accessory,
  };

  nftsCollection.push(nft);
}

function listNFTs() {
  nftsCollection.forEach((nft, index) => {
    console.log(`NFT ${index + 1}:`);
    console.log(" CName: " + nft.name);
    console.log("Hairolor: " + nft.hairColor);
    console.log("Shirt Type: " + nft.shirtType);
    console.log("Accessory: " + nft.accessory);
    console.log("------------------");
  });
}

function getTotalSupply() {
  return nftsCollection.length;
}

mintNFT("New NFT 1", "Red", "Hoodie", "Earrings");
mintNFT("New NFT 2", "Blue", "T-Shirt", "Bracelet");
mintNFT("New NFT 3", "Green", "Button-Up Shirt", "Diamond Ring");

listNFTs();
console.log("Total NFTs: " + getTotalSupply());
