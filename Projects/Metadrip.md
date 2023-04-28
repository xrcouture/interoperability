# Metadrip

<img src="https://user-images.githubusercontent.com/122074866/235122574-f97ea968-7290-4959-816e-8d3c8b4d156a.png" width="100%"/>

## What is Meta Drip?
A collection of 12 designs created by independent artists using different softwares and design principles. Each design has unique attributes/properties from material type, pattern style, silhouette and more.
The collection was created with an aim to make it accessible in as many web2 and web3 platforms as possible and give its NFT holders exclusive access.

[You can check the live collection here!](https://metadrip.xrcouture.com) 

[You can check the 3d technical process here](https://metadrip.xrcouture.com)

Current distribution of Meta Drip
12 designs x 10 supply = **120 NFTs**
Minted = 71 NFTs
Available = 49 NFTs

---

## Why Metadrip

We wanted to start with a small collection to explore designs that are challenging and different in texture, material, shape and form. We wanted  to see how closely this type of a collection can be created for different platforms while maintaining the fidelity and feel of the original to whatever possible extent.

---

## Our Goal

We look at this project as an experimental collection to explore all possible avenues of creating an interoperable wearable that can seamlessly be taken into different metaverses along with all the traits, bells and whistles that the original NFT would promise. 
We are exploring different workflows and integrations to make the best use of current systems and also explore the development of better and easier systems of working for both the creators and the users.

---

## Metadrip roadmap:

Keeping in mind the technical constraints and challenges of what is possible today versus what might be possible tomorrow, we’ve divided our roadmap into three milestones.

---

## Metadrip 1.0
<img src="https://user-images.githubusercontent.com/122074866/235123629-678d42e9-a94a-4e42-9236-a7917f701c7c.png" width="100%"/>

### Stage: Complete

### Goal: To solve for users
  
  Offer an interoperable wearable to the user where they can explore a cohesive identity across multiple metaverses and take their assets across platforms

### Achievement

**A]** We successfully deployed a collection of 12 wearable NFT’s and released it to the public for minting. 

Added in utilities and deployed the collection for compatibility with platforms like: 
  1) Decentraland
  2) Snapchat AR
  3) Zepeto
  4) Minecraft
  5) Megaverse
  6) Clonex
  7) Ovr
  
And created for other platforms like:
  1) Roblox
  2) Sandbox
  3) Zepeto
  4) Minecraft
  5) Monaverse
  6) Megaverse
  7) Vroid VRM
  8) Clonex
  9) Metahuman

<img src="https://user-images.githubusercontent.com/122074866/235130642-43a1e6fe-ec49-4653-b191-d3cc63e4e9e5.png" width="100%"/>
We’ve documented all the technical aspects of creating 3d wearable [here](https://)


**B]** We’ve tried to use each platform's unique capabilities to enhance the experience of using the wearable natively in that platform. 
For example- We’ve added blinking lights using shader manipulations in Lens studio to create a more vivid experience for snapchat users to try on the Dazzling devil wearable

https://user-images.githubusercontent.com/122074866/235131276-5bfbdd56-c082-4511-9612-89847c3a2b75.png

See how one wearable looks when taken different platforms [here](https://)
See the process of creating for different AR platforms [here](https://)

**C]** We’ve researched and successfully deployed linked wearables through API’s provided by Decentraland and OVR and have started exploring other ways to create a seamless verification process for NFT holder’s 
 
### Learnings: 
  - Creating 3d assets which are compatible for various platforms is a time consuming and tedious process
    [We’ve drawn a more streamlined process for creating 3d assets here](https://)
  - Verification methods for an ownership of an NFT on different platforms is clunky since all platforms function on different blockchains
  - Integrations with different platforms requires some kind of an API which allows us to do so – which in most cases metaverses currently don't provide
  
---

## Metadrip 2.0 

### Stage: in development

### Goal: To solve for Metaverse platforms

  Highlighting the problem of collaborating with different metaverse platforms seamlessly where the option of NFT verification and the 3d assets be usable and seamless.
In order to do so, 
  - We have decided to make the project ‘open-source’ to encourage exchange of resources and community participation while contributing our findings to help with the   research.
  - We wish to work with forums such as ‘Metaverse Standard Forum’ to align with standards, research work from industry leaders
  
### Achievement: 
So far we have collaborated with megaverse which is on the polygon blockchain and deployed our metadrip collection on the platform using our API to directly verify NFT holders on the platform and seamlessly use our wearables for their avatars directly on connecting their wallets.

You can read more about our API [Here](https://)
You can view the megaverse project and know more [here](https://)

---

## Metadrip 3.0

### Stage: brainstorming

### Goal: 

To solve for 3d artists
Create a system/ tool /standard where an asset needs to only be created once and then can be taken into different platforms.

### Ideas:

  The creation of 3d assets is time consuming, mostly repetitive when done for different platforms. We hope to ease this process for the creators so the community can grow as a whole. 
  
  If we just brainstorm on what the solution could look like , these 2 roadmaps seem to emerge broadly. We think the solution largely would be a combination of both.
  

**A]**  A tool that understand the way each platform avatar works and categorize them on the basis of mesh/voxel/sprite sheet/2d
  - That can efficiently read different body type standards from different platforms and deform the 3d asset according to those body types while automatically rigging and skinning the asset according to the shape and proximity of the wearable meshes from the rig.

Some tools with interesting workflows in this context:

[Auto fitting capabilities in marvelous designer](https://)
 
<img src="https://user-images.githubusercontent.com/122074866/235134913-07d3fa80-8a77-4b5c-a9e4-6e8a6ca7a108.png" width="100%"/>
 
[Layered clothing concepts from Roblox](https://)
 
<img src="https://user-images.githubusercontent.com/122074866/235135355-18560dd3-be3b-4e66-af55-dc30866370bd.png" width="100%"/>
 
[Voxel heat diffused skinning plugin in blender](https://)
 
<img src="https://user-images.githubusercontent.com/122074866/235135527-9575debd-7684-42c6-9e45-b52c3ebe7d01.png" width="100%"/>

  - If the target platform is voxel based- It should know how to assign and simplify the meshes to achieve that voxel look with the appropriate voxel resolution needed for the platforms, while assigning appropriate colors to the geometry.
  - With capabilities to accurately render sprite sheets in different styles/ requirements
  - With capabilities of mesh optimization according to the fidelity of the desired platforms
  - With capabilities of understanding different shader types of different platforms and creating relevant material setups for each for best possible quality and visuals.
  - With export capabilities that can format the textures, naming conventions/ and other specifics according to the platforms requirements.

Something like this will cover the bare basics of creating a 3d wearable asset for different avatars across platforms. But with NFT’s there is an added layer of rarity that in a lot of cases is powered by certain capabilities in games- like a wearable that allows you to fly in one metaverse might need an equivalent capability in another.

Also with AI and tech continuously advancing, if we were to think about how wearables in the future would look like, It’s interesting to imagine concepts on how interactions in the metaverse would function and what it may look like. For example emotion dependent visual effects with wearables.

[Here’s a small discussion where we’ve visualized  how a wearable of the future might  look like and the capabilities it might have](https://)



**B]** The second solution can be a filetype which can be a standardized solution across all metaverses such a filetype may bake in all the necessary information that the asset might need to function well in any platform, including all the metadata it needs to be compatible and make use of all the features native to that platform.


We have seen VRM as a very versatile format in this regard since it allows the users to add in a lot of interesting features/ interactions to the avatars like- deform bones, particle effects as well as blendshapes, etc. 

https://user-images.githubusercontent.com/122074866/235131276-5bfbdd56-c082-4511-9612-89847c3a2b75.png

But the major constraint here is that it is an avatar standard and does not allow easy customizability for the outfit/skin color/hair etc.

There are a lot of easy creator tools that have simplified the process of creating VRM’s like VROID, but are very limited and still not as intuitive for any average user.

[You can view some of our experiments where we take one VRM avatar and explore how it can be taken across platforms](https://)


All this led us to experiment with creating an easy wearable editor for VRM and GLTF avatars.

We want a simple drag and drop interface that allows users to upload any avatar and dress it with our wearables.

We’ve started the development with support for Clonex avatars.Eventually we plan on adding support for multiple body types

[You can learn more about it here](https://)

---

## Notes:
**We are constantly exploring more tools and processes to help us move closer to the truly interoperable wearables in the metaverse. We hope to collaborate with creators and platforms in the process 🙂**

---

## How to contribute: 






  


