## 3d development process- Multiple platforms


<img src="https://media.discordapp.net/attachments/1087307130958250004/1104303125998862346/Streamline_Process_AdobeExpress.gif" width="100%"/>

## Overview

Creation of 3d garments is a multi step process. There are many ways to go about the creation process in 3d since there are a lot of tools out there, and many more workflows.
The below mentioned workflows are what work best for us.

There are 2 main ways of creating a 3d garment- dependent on the target platform and what it supports:

Mesh based
Voxel based

## Mesh based Process

## Process can be divided into 2 parts:

## A]. Mesh creation and prep 

<img src="https://user-images.githubusercontent.com/122074866/236602000-790fbcbf-87f3-42d1-9cbf-cf566c8f3ef1.png"/>

## Marvelous/ Clo3d
The 3d creation process starts with the creation of the 3d asset in Clo3d/ Marvelous designer.

<div align="center">
<img src="https://user-images.githubusercontent.com/122074866/236602071-07d419ca-66f6-440f-bb3c-b6185f1bdb1e.png"/>
</div>

## Retopology

It is then taken into blender/ any 3d software for retopology and optimization. It’s best to have an optimum poly count in this with a good edge flow so the files can be easily edited later according to the requirement of the specific platforms.

<div align="center">
<img src="https://user-images.githubusercontent.com/122074866/236602176-73dbe161-6313-481b-b91e-dfb3e4f4c7ab.png"/>
</div>


## UV Unwrapping:


<div align="center">
<img src="https://user-images.githubusercontent.com/122074866/236602284-a0b5230f-008a-4971-8cc7-7936091f65ad.png"/>
</div>

Example of good edge flow:

<img src="https://user-images.githubusercontent.com/122074866/236602421-eba977c7-9086-41b6-abb5-b82cf7dbdcfd.png"/>

## Texturing and baking

<img src="https://user-images.githubusercontent.com/122074866/236602468-7017d95b-eced-4319-982b-ffab2a2e44b9.png"/>


Once the asset is created, we need to rig it using a simple rig. In the image below we’ve used blender’s meta rig. This is just so we can pose the garment easily according to the desired base skeleton for any platform. 

<img src="https://user-images.githubusercontent.com/122074866/236602578-9f265867-757c-4124-92e0-910257310876.png"/>


## B]. Platform specific processes:
## Here we explore the process of creating for 4 different platforms:


## 1. Decentraland

<img src="https://user-images.githubusercontent.com/122074866/236602723-07ec6d11-ee91-444e-9c07-dc39adc0ed52.png"/>

## Rig matching to DCL Rig:
W now need to pose the character according to the base pose dor the Provided rig and body shape of decentraland

The DCL Body base mesh comes in a male and female body type which is further divided into parts:

<div align="center">
<img src="https://user-images.githubusercontent.com/122074866/236602917-e9546b5a-3abf-439f-90d0-cca2184b4fe3.png"/>
<img src="https://user-images.githubusercontent.com/122074866/236602918-999eb748-a80d-4ae4-a3e1-3ed04d03ceeb.png"/>
<img src="https://user-images.githubusercontent.com/122074866/236602920-b7fe3fd8-2e36-4a29-af77-b4dfdb03f309.png"/>
</div>

This means we need to create the garment in such a way that it does not clip through the mesh. Usually we start with the female body type since it has a wider hip area.

Chrome heart posed:

<div align="center">
<img src="https://user-images.githubusercontent.com/122074866/236603227-51b0e23d-809a-40c8-ba05-09f66293b73e.png"/>
</div>


## Mesh Optimization:

<img src="https://user-images.githubusercontent.com/122074866/236603356-75f88c61-9c65-4663-a097-f5f864af6c54.png"/>

Based on these categories, We need to decide the target poly counts for the respective meshes
  - No more than 1.5K triangles per wearable slot: hat, helmet, upper body, lower body, feet and hair.
  - No more than 500 triangles per category: mask, eyewear, earring, tiara, top_head and facial hair.
  - No more than 2 textures (at a resolution of 512x512px or lower) per wearable. All textures must be square at 72 pixel/inch resolution.
  - No more than 2 materials (without counting the AvatarSkin_MAT)
  - In the case of skin wearable, the amount of tris allowed are 5k and 5 textures.

   Simplifies meshes:

<div align="center">
<img src="https://user-images.githubusercontent.com/122074866/236603465-06ecc4fa-e488-4e0f-b6a5-2784c1876716.png"/>
</div>

<div align="center">
<img src="https://user-images.githubusercontent.com/122074866/236603538-ec0dffb8-d071-46f8-ac0f-606a0a1e69db.png"/>
</div>

After the meshes are retopologized, we need to take care that all the faces are facing outwards since DCL only renders one side of the face

<div align="center">
<img src="https://user-images.githubusercontent.com/122074866/236603590-762e9ed3-7d31-4907-98c3-fb0373f4eb92.png"/>
</div>

## Weight painting to the new rig
We need to make sure all the weights are assigned to each bone properly so there are no clipping issues.

<div align="center">
<img src="https://user-images.githubusercontent.com/122074866/236603655-f158d85a-1721-4813-85da-0e3ca4359758.gif"/>
</div>

<div align="center">
<img src="https://user-images.githubusercontent.com/122074866/236604265-c1b2cb8d-7162-4813-a6d8-7778ec5a30b8.gif"/>
</div>

## Simplify materials

  Decentraland wearables currently supports 3 types of maps, which are:
  - Base Color: This is the main texture with the colors and details of your model.
  - Emission: This map is for the parts that are glowing in your model. The emission map goes in a separated material specifically for emission.
  - Alpha: This map is to handle transparency. It uses the opacity channel of the texture. (It is always preferable to use Alpha Clip rather than Alpha Blend, using a black and white texture for the cutout)


## Exporting as glb

<div align="center">
<img src="https://user-images.githubusercontent.com/122074866/236604767-7cc5bda2-091f-4e30-9b5f-a9bc1f18da7d.png"/>
</div>

Upload to DCL Builder

<div align="center">
<img src="https://user-images.githubusercontent.com/122074866/236605300-b5100cfa-38b8-4190-a0b5-04713be9860e.png"/>
</div>

## Configure settings

<div align="center">
<img src="https://user-images.githubusercontent.com/122074866/236605728-5acfed8a-ed54-42b3-8fe3-680cad98d3ef.png"/>
</div>

After all this we can Hit publish!

[For more info, check the Decentraland docs](https://docs.decentraland.org/creator/wearables/creating-wearables/)


---


##  2. Roblox
   Roblox has 2 different workflows- one is layered clothing and other is classic clothing. Here is the process overview for creation:

<div align="center">
<img src="https://user-images.githubusercontent.com/122074866/236605894-d32266e7-54fa-4c4b-aa3e-c0476dfd8088.png"/>
</div>

## 2.1) Layered clothing process:

Roblox provides a base avatar and skeleton file which has a unique layering system of 2 meshes. Inner and outer mesh. We need to Fit the garment such that it lies between the inner and outer mesh. The reason for this is to fit any avatar type using layers. Here how that looks like

<div align="center">
<img src="https://user-images.githubusercontent.com/122074866/236605951-c0e60078-6262-4d60-beda-da36dfc594fe.png"/>
 </div>

<div align="center">
<img src="https://user-images.githubusercontent.com/122074866/236606006-a9da7490-f5e5-40f3-83b9-9a6b91414341.png"/>
</div>

Another point to note is that there are attachment points given in the base file so that things like swords/belts. Accessories etc. can be attached. 
We might need to shift these attachment points according to our garment

Inner cage with deformed mesh and attachment points placed.

<div align="center">
<img src="https://user-images.githubusercontent.com/122074866/236606039-8c8df54e-8a52-4887-9e6f-781d6415a077.png"/>
</div>

Edited outer to fit the skirt area:

<div align="center">
<img src="https://user-images.githubusercontent.com/122074866/236606084-8cf2ec74-3f3f-4a26-96aa-28bbb88778da.png"/>
</div>

This can now be exported as an FBX for roblox studio

In roblox studio we need to Configure the materials and test for deforms. We also have the ability to edit the mesh a little using a lattice structure within roblox studio itself. 
Refer the link below for more details

[https://create.roblox.com/docs/avatar/accessories/accessory-fitting-tool](https://create.roblox.com/docs/avatar/accessories/accessory-fitting-tool)

<div align="center">
<img src="https://user-images.githubusercontent.com/122074866/236606182-e7a728ea-809f-400d-a604-c374cf7ace42.png"/>
</div>

Here’s a preview of chrome heart in roblox:

## Classic clothing

Classic clothing is a type of 2D cosmetic item that you can apply to the surface of an avatar character.

<div align="center">
<img src="https://user-images.githubusercontent.com/122074866/236606219-9e13e9c5-cc96-4445-80ad-d99da3e28417.png"/>
</div>

Here's more on how to create it:
[https://create.roblox.com/docs/avatar/accessories/classic-clothing](https://create.roblox.com/docs/avatar/accessories/classic-clothing)


---



## 3. Zepeto

<img src="https://user-images.githubusercontent.com/122074866/236606293-705e21d8-63be-4f52-8f48-2c908bab4c86.png"/>


## Rig and pose matching

<img src="https://user-images.githubusercontent.com/122074866/236606346-39bbcf12-9175-4e60-9362-6f27cd64b55b.png"/>

<img src="https://user-images.githubusercontent.com/122074866/236606353-f811f19a-2b7b-42c6-9b89-df3d79bba928.png"/>

<img src="https://user-images.githubusercontent.com/122074866/236606417-a6331273-d67b-477e-b954-b4b109606e35.png"/>

<img src="https://user-images.githubusercontent.com/122074866/236606692-1fb4508c-db1d-45ab-8d70-812ca9f19e1c.png"/>


Mask Painting

<div align="center">
<img src="https://user-images.githubusercontent.com/122074866/236607339-013d8a05-494c-4678-ba41-2f75ab256538.png"/>
</div>

Rigging and weight painting

<div align="center">
<img src="https://user-images.githubusercontent.com/122074866/236607383-96f65e3f-0324-495b-935a-d5d482cc99df.png"/>
</div>

<img src="https://user-images.githubusercontent.com/122074866/236607424-f7436f7f-c5d3-41a6-8960-e6682afd24ce.png"/>

## Export as FBX

Import into unity and follow the steps given here.
[Unity edits](https://docs.zepeto.me/studio-item/lang-ko/docs/converting_export)

Zepeto provides a unity package that helps with the conversion process to make all the changes. The main aim is to configure the materials and test for the different body types. 

<img src="https://user-images.githubusercontent.com/122074866/236607541-1d4b8d36-1abb-49ab-8a06-32461baff4fd.png"/>







## Voxel Based Process

There are many voxel based editors out there, but the best way to create for sandbox is to use the editor they have developed- It’s called Vox edit. 
## Sandbox

<img src="https://user-images.githubusercontent.com/122074866/236607606-19cae4bb-8fca-41eb-94f5-911abd2eba22.png"/>

## New Avatar

<img src="https://user-images.githubusercontent.com/122074866/236607647-84411e5c-b3ef-49f9-bb94-735bdbce2600.png"/>

## Creating Voxel Geometry

Creating voxels in vox edit is very much like painting in 3d using blocks. 
<img src="https://user-images.githubusercontent.com/122074866/236607700-9b46a214-6dc6-4088-98e7-b7860da1f53a.png"/>

<img src="https://user-images.githubusercontent.com/122074866/236607735-2c299214-9918-4f46-9d5e-fe5b22e24e95.png"/>

## Glow materials(Emissive)
Vox edit has the ability to add emissive materials. You can do that by enabling this opinion

<div align="center">
<img src="https://user-images.githubusercontent.com/122074866/236607816-6fe266e9-f830-4922-bc66-6cc22ad306e5.png"/>
</div>

## Export to sandbox Marketplace

<img src="https://user-images.githubusercontent.com/122074866/236607854-4d07822a-2879-4a28-abf7-fdab2fb56870.png"/>

## Configure Settings

Each avatar has a set of rarities. While exporting we have the option of editing these 

<img src="https://user-images.githubusercontent.com/122074866/236607897-14e73a0d-f89e-42af-86a3-cfbc2e35aab7.png"/>

## Testing

Once everything is built , it's a good practice to test out how the avatar functions in the game. We can do this by testing it in the game editor. 

<img src="https://media.discordapp.net/attachments/1081164227890384907/1104345506546720808/image32.gif?width=800&height=450"/>

Once it’s all good, 
we are all set to publish!


## Streamlining the process of creation:

These were 4 different platforms that broadly explain the process for creating for various platforms/types.

We can avoid repetitive work in creating for multiple other platforms if we know all the target steps, parameters and poly counts. 

Here’s a comparative view for the parameters for different platforms:

<img src="https://user-images.githubusercontent.com/122074866/236608018-39a2d782-4c85-41f8-84b2-463fae3596b1.jpg"/>


Moreover there are other platforms that are overall similar to these 4 platforms. To create compatible meshes in a more streamlined way, we can take some common points and create for various other platforms too to streamline it further. 




## Resources: 

[https://sandboxgame.gitbook.io/the-voxedit-academy/voxedit/welcome-to-the-voxedit-academy](https://sandboxgame.gitbook.io/the-voxedit-academy/voxedit/welcome-to-the-voxedit-academy)

[https://sandboxgame.gitbook.io/the-sandbox/links-and-resources/tutorials](https://sandboxgame.gitbook.io/the-sandbox/links-and-resources/tutorials)

[https://docs.decentraland.org/creator/wearables/wearables-overview/](https://docs.decentraland.org/creator/wearables/wearables-overview/)

[https://create.roblox.com/docs/resources/beyond-the-dark/layered-clothing](https://create.roblox.com/docs/resources/beyond-the-dark/layered-clothing)

[https://docs.zepeto.me/studio-item/lang-ko/docs](https://docs.zepeto.me/studio-item/lang-ko/docs)









