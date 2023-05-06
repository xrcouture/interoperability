# 📙 API Documentation

Welcome to the documentation of the api that is used to achieve interoperability of digital fashion wearables across different platforms. This documentation is mainly focused on the existing metadrip NFT collection


<div align="center">
  <img src="https://user-images.githubusercontent.com/122074866/236494734-5c0b0e0a-395d-477e-be43-c8b782518e1e.png" width="auto"/>
</div>

---

## 🥅 Goal

To achieve interoperability of digital fashions wearables across web2 and web3 platform

---

## 🔗 Web2 and Web3 platforms

  The platfroms allow their users to import the digital fashion wearables that are minted/created outside their environment to use it in their environment. The users can connect their wallet(web3) or email(web2) in these platforms and retrieve all their purchased NFTs. This solves the metaverse problem of interoperability. Also this approach connects web2 and web3 platforms together, which allow more web2 users onboarding to web3

---

## Why 
  This API largely solves the problem of interoperability. It connects multiple platforms together and allow them to access each other wearables. 
  The integration of this API in the platform allows expanded offering to it's users, which in turn makes more user to explore the platform where they can use their existing wearables.
  This serves as an entry to the "Open Metaverse". 

---

## What is the benefit of using the API
  The API provides seamless and easy integration with the platforms. The API paves way to integrate your digital fashion wearables purchased from a marketplace or an in-Game purchase to be used across different platforms no matter about their formats. A win-win solution for both the platform and XRC by this approach and it creates additional revenue flow.
  
---

## 🖼️ Origin NFT

  We are not going to mint separate NFTs for each platform, instead mint a single NFT known as **Origin NFT** and link multiple 3d assets and it's schema to it. 
An ownership of the NFT means, the collective ownership of the wearables in all its linked metaverse/web2 platform

  The ownership of NFT can be transferred to other user, which means the new owner has access to the wearables in all these platforms. 
It is not possible to transfer ownership of a wearable for one particular platform.

---

## Who can use this API

  Any Metaverse / Web2 platform that want to support interoperable digital fashion assets can start using this API. You can straightaway use this api, if your wearables 3d specifications matches any of the supported platform mentioned below. If not, we can customize the 3d files for your specifications
  
---
  
## Supported integrations
  There are two ways by which the metaverse platforms can integrate their platform with XRC
  - REST API (Web2 and Web3)
  - Unity SDK

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

## Unity SDK

  We are also working on a Unity SDK, that can be imported into the environment. To know more about this, [contact us](mailto:hello@xrcouture.com)
  
  
## Supported Platforms

<div align="center">
      <img src="https://media.discordapp.net/attachments/1087307130958250004/1104027761993060372/Group_6.png?width=1001&height=532">
</div>

  Below are the list of supported platforms for the metadrip collection

    1) Decentraland
    2) Zepeto
    3) OVR
    4) Snapchat
    5) Roblox
    6) Sandbox  
  
# Support

  If you are facing any issues in integrating the API, please feel free to [book a meeting](https://calendly.com/rakesh-xrc/30min) with us.


