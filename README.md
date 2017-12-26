# Ethereum-Address-Alert-Bot
simple tool to watching an ether address if any ETH transactions coming in...


Why this is useful? there are many Ether address are public for testnet, but people make mistack and sending ETH to those addresses at mainnet.
Then you might want to watching out those public known wallet, if any transactions comes in it is Free ETH for you LOL.


For example: 
(5) 0x2932b7a2355d6fecc4b5c0b6bd44cc31df247a2e
(6) 0x2191ef87e392377ec08e7c08eb105ef5448eced5
(7) 0x0f4f2ac550a1b4e2280d04c21cea7ebd822934b5
(8) 0x6330a553fc93768f612722bb8c2ec78ac90b3bbc
(9) 0x5aeda56215b167893e80b4fe645ba6d5bab767de

Private Keys:
(5) 659cbb0e2411a44db63778987b1e22153c086a95eb6b18bdf89de078917abc63
(6) 82d052c865f5763aad42add438569276c00d3d88a2d062d36b2bae914d58b8c8
(7) aa3680d5d48a8283413f7a108367c7299ca73f553735860a87b08f39395618b7
(8) 0f62d96d6675f32685bbdb8ac13cda7c23436f63efbb9d07700d8669ff12b7c4
(9) 8d5366123cb560bb606379f90a0bfd4769eecc0557f1b362dcae9012b548b1e5


With cjs extension for chrome add the following:

```javascript

$(function(){
   var pending = $('#transactions table i:contains("pending")').length;
   if(pending > 0){
        console.log('WOW --> ' + pending);
        var obj = document.createElement("audio");
        obj.src="http://www.noiseaddicts.com/samples_1w72b820/3720.mp3";
        obj.volume=0.10;
        obj.autoPlay=false;
        obj.preLoad=true; 
        setInterval(function(){
            obj.play();
        }, 500);
   } else {
       setTimeout(function(){
            location.reload();
       }, 15000);
   }
});

```
Test on the following URL:

https://etherscan.io/address/0xfbb1b73c4f0bda4f67dca266ce6ef42f520fbb98

if there is a pending transaction, a dog bark sound will be played.
