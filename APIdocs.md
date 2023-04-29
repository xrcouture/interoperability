# 📙 API Documentation

Welcome to the documentation of the api that is used to achieve interoperability of digital fashion wearables across different platforms. This documentation is mainly focused on the existing metadrip NFT collection

![ezgif com-video-to-gif](https://user-images.githubusercontent.com/122074866/234850975-50f66b94-4833-448f-8f58-0bc3f16a37aa.gif)

---

## 🥅 Goal

To achieve interoperability of digital fashions wearables across web2 and web3 platform

---

## 🔗 Web3 platforms

  The platfroms allow their users to import their digital fashion wearables that are minted/created outside their environment to use it in their environment. The users can connect their wallet in these platforms and retrieve all their purchased NFTs
  
## 🎮 Web2 platforms

  The Web2 Games or platform also can allow their users to import their digital fashion wearables in to their environment. The users can connect using the email address to retrieve the assets that are linked to that particular email Id and use that in the environment  To know more about it. Book a demo with us

---

## 🖼️ Origin NFT

  We are not going to mint separate NFTs for each platform, instead mint a single NFT known as **Origin NFT** and link multiple 3d assets and it's schema to it. 
An ownership of the NFT means, the collective ownership of the wearables in all its linked metaverse/web2 platform

  The ownership of NFT can be transferred to other user, which means the new owner has access to the wearables in all these platforms. 
It is not possible to transfer ownership of a wearable for one particular platform.

---

## API

  The platforms will be provided with a REST API and these platforms can use it to retrieve the wearables/digital fashion asset and show it in their own marketplace or under users profile in the metaverse. We are also working on a Unity based SDK that can be directly integrated within the environment
  
  
<div align="center">
      <img src="https://user-images.githubusercontent.com/122074866/234560521-49e9574a-0ecc-4322-9e83-11342ba989ab.png">
</div>

# Format

https://api.model.metadrip.xrcouture.com/web3/v1/{apikey}/platform/{platformName}/address/{walletAddress}

Example

https://api.model.metadrip.xrcouture.com/web3/v1/xrc-abcdefghijklmnopqrst/platform/decentraland/address/0xcd8c097cC2331EeF50074bf69F7eD26e7896D48b

# Response
The response to this request will in Json format


<div align="center">
      <img src="https://user-images.githubusercontent.com/122074866/234604017-075b4c34-4956-4bbb-ac96-26373400f3a1.png">
</div>

## Supported Platforms

1) Decentraland
2) Zepeto
3) OVR
4) Snapchat
5) Roblox
6) Sandbox

## Who can use this API

  Any Metaverse / Web2 platform that want to support interoperable digital fashion assets can start using this API. You can straightaway use this api, if your wearables 3d specifications matches any of the above supported platform. If not, we can customize the 3d files for your specifications



