# 📙 API Documentation

Welcome to the documentation of the API that enables interoperability for digital fashion wearables across various web2 and web3 platforms. This documentation will help you understand the features and functionalities of the metadrip NFT collection, which consists of 12 unique and creative wearables for your avatars designed by independent creators. Metaverse platforms can install this API for free and contribute to the vision of an interoperable and open metaverse, where users can enjoy the freedom and diversity of digital fashion. Join us in this exciting journey to create the metaverse of tomorrow!


<div align="center">
  <img src="https://user-images.githubusercontent.com/122074866/236494734-5c0b0e0a-395d-477e-be43-c8b782518e1e.png" width="auto"/>
</div>

---

## 🥅 Goal

With this API we wish to,
- Promote 'Open-Metaverse' and '3D Standards'
- Document various industry standards for wearabales and avatars:
- Allow users to make digital fashion fun and easy to use, no matter what platform they are on.
- Enable creators to showcase thier work and reach more people with interoperable wearables.
- Enable interoperability and bring-in more users and creators for metaverse platforms
- Tap into the larger web2 audience and incentives them to explore new web3 pltaforms. Thus, onboarding new users to web3.

---

## Benefits of using the API

- API makes it simple and seamless to use digital fashion wearables on different platforms.
- Create Origin NFTs that link multiple assets under one schema, a better alternative to Aridrops.
- Provide additional value for users, and opputunity to attract NFT holders. 
  
---

## Who can use this API

  Any web2 or web3 metaverse platform that want to support interoperable digital fashion assets can start using this API. You can straightaway use this api, if your wearables 3d specifications matches any of the supported platform mentioned below. If not, we can customize the 3d files for your specifications
  
---
  
## Supported integrations

  There are two ways by which the metaverse platforms can integrate their platform with XRC
  - REST API (Web2 and Web3)
  - Unity SDK
  - Unreal Engine SDK

---

## REST API (Web3)

  The platforms will be provided with a REST API and these platforms can be used to retrieve the wearables/digital fashion asset and show it in their own marketplace or under users profile in the metaverse.
  
  
<div align="center">
      <img src="https://user-images.githubusercontent.com/122074866/234560521-49e9574a-0ecc-4322-9e83-11342ba989ab.png">
</div>

### Access and authentication
  All API request is sent over HTTPS and accessed from https://api.model.metadrip.xrcouture.com
  
  The API access is restricted and it needs an API key to access it. You can generate a key [here](https://metadripos.netlify.app/api)

### Format
  The API request should be in below format

  <img src="https://img.shields.io/static/v1?label=&message=GET&color=blue"> https://api.model.metadrip.xrcouture.com/web3/v1/{apikey}/platform/{platformName}/address/{walletAddress}
  
  where,
  
   - {apikey} => unique key to access the api
    
   - {platformName} => platformName from the list of supported platforms mentioned below in the document
   
   - {walletAddress} => wallet address of the owner of the metadrip collection

  Example

  https://api.model.metadrip.xrcouture.com/web3/v1/xrc-abcdefghijklmnopqrst/platform/decentraland/address/0xcd8c097cC2331EeF50074bf69F7eD26e7896D48b

### Response
The response to this request will in Json format


  ```json
  [
    {
      "name": "Dazzling Devil",
      "description": "Straight from the streets of LA, the mind-blowing outfit by Lucii is ready to give your virtual closet a blend of futuristic and gala vibes. The multi-colored flashlights, the leather finesse, and the ‘ready-to-rock’ boots underline the designer’s cutting-edge creativity and imagination. Be the multi-hued spotlight in the Metaverse!",
      "image": "https://nft.xrcouture.com/artgallery/phase2/Lucii/3.png",
      "animation_url": "ipfs://bafybeieqtrzqyk4nawljawdgd5vfmv5wtcnmfxewlyanznvyecltdrb47q",
      "id": {
        "platform": "decentraland",
        "chain": "matic",
        "address": "0x99d6c0d1a656a1ee1f345ae6482d0afd76daf8a5"
      },
      "wearables": "https://metadrip.xrcouture.com/*******/*********/Dazzling_Devil_DCL.glb",
      "category": "Upper Body"
    }
  ]
  ```

## REST API (Web2)

  The web2 platforms will be provided with a REST API and these platforms can pass the users email address in the API to get the users assets
  
### Format
  
  The API request should be in below format

  <img src="https://img.shields.io/static/v1?label=&message=GET&color=blue"> https://api.model.metadrip.xrcouture.com/web2/v1/{apikey}/platform/{platformName}/email/{emailAddress}
  
  where,
  
   - {apikey} => unique key to access the api
    
   - {platformName} => platformName from the list of supported platforms mentioned below in the document
   
   - {emailAddress} => email address of the user who owns the asset

  Example

  https://api.model.metadrip.xrcouture.com/web2/v1/xrc-abcdefghijklmnopqrst/platform/decentraland/email/abc@xyz.com
  
  ### Response
The response to this request will in Json format


  ```json
  [
    {
      "name": "Dazzling Devil",
      "description": "Straight from the streets of LA, the mind-blowing outfit by Lucii is ready to give your virtual closet a blend of futuristic and gala vibes. The multi-colored flashlights, the leather finesse, and the ‘ready-to-rock’ boots underline the designer’s cutting-edge creativity and imagination. Be the multi-hued spotlight in the Metaverse!",
      "image": "https://nft.xrcouture.com/artgallery/phase2/Lucii/3.png",
      "animation_url": "ipfs://bafybeieqtrzqyk4nawljawdgd5vfmv5wtcnmfxewlyanznvyecltdrb47q",
      "id": {
        "platform": "roblox",
        "email": "abc@xyz.com"
      },
      "wearables": "https://metadrip.xrcouture.com/*******/*********/Dazzling_Devil_DCL.glb",
      "category": "Upper Body"
    }
  ]
  ```

## Unity/ Unreal Engine SDK

  We are also working on a Unity SDK, that can be imported into the environment. To know more about this, [contact us](mailto:hello@xrcouture.com)
  
  
## Available 3D formats

  Below are the list of 3D formats crated as per the standards of popular web2 and web3 platforms, that you can access using the API.

<div align="center">
      <img src="https://media.discordapp.net/attachments/1087307130958250004/1104027761993060372/Group_6.png?width=1001&height=532">
</div>

    1) Decentraland
    2) Zepeto
    3) OVR
    4) Snapchat
    5) Roblox
    6) Sandbox  
  
# Support

  If you are facing any issues in integrating the API, please feel free to [book a meeting](https://calendly.com/rakesh-xrc/30min) with us.


