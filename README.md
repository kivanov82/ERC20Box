# ERC20Box
ERC-721 token that wraps a portion of ERC-20

The idea is to have a sort of the tradable and transferrable loot-box, which holds a portion of ERC-20 tokens inside.

**Create**

The token owner decides on how many ERC-20 tokens are put into each box token, calling the ERC20Box constructor.
After, the owner must deposit (but first *approve* in the ERC-20) ERC-20 into the ERC20Box. In it's turn, the Box will mint a number of NFTs to the owner.

**Transfer**

When the boxes are created, they can be transfered/sold/bought similar to the standard ERC-721.

*Good to know:* ERC20Box is fully compatible with the OpenSee market http://opensea.io and can be listed there

**Use**

In order to receive the box's content, the owner must 'open' it, calling 

`unpack(tokenId)`

method. This will deposit ERC-20 tokens to the opener, and burn the box token.
