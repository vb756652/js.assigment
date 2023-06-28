// create a variable to hold your NFT's
const NFTs = [];
// this function will take in some values as parameters, create an
// NFT object using the parameters passed to it for its metadata, 
// and store it in the variable above.
function mintNFT (_name, _city, _age, _cloth, _clothColor) {
    const NFT = {
        "name" : _name,
        "city" : _city,
        "age"  : _age,
        "cloth": _cloth,
        "clothColor": _clothColor,
    }
    NFTs.push(NFT);
    console.log("Minted :" + _name);

}

// create a "loop" that will go through an "array" of NFT's
// and print their metadata with console.log()
function listNFTs () {
    for(let i = 0; i<NFTs.length; i++){
        console.log("\nID  :\t\t" + i+1);
        console.log("Name :\t\t" + NFTs[i].name);
        console.log("City :\t\t" + NFTs[i].city);
        console.log("Age  :\t\t" + NFTs[i].age);
        console.log("Cloth :\t\t" + NFTs[i].cloth);
        console.log("Cloth Color:" + NFTs[i].clothColor);
    }

}

// print the total number of NFTs we have minted to the console
function getTotalSupply() {
    console.log("\n"+NFTs.length);

}

// call your functions below this line
mintNFT("Young","Mumbai","20","Shirt","Blue");
mintNFT("Angle","Pune","17","T-Shirt","Yellow");
mintNFT("Zubair","Chandigarh","25","Shirt","Light Green");

listNFTs();
getTotalSupply();

