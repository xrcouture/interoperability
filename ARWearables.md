## Creating AR Wearables with snapchat

<div align="center">
  <img src="https://user-images.githubusercontent.com/122074866/236392211-9c75a90c-b8c8-4d41-9ee6-1e58ff7e57c7.gif"/>
</div>

## Intro

We’ve been developing various games and metaverses. But with AR the ways of creating and experiencing are slightly different.
It’s an interface that we see through the camera. So the possibilities in AR are very much tied to the hardware that is commonly available for users to experience , as well as what the camera and sensors can see. 


Current technologies have come far with ML models working in the backend to allow for human body tracking just through detection from the camera feed! 

Interactions in AR also play very differently as compared to games.Since the camera sees the real world, there are a lot of opportunities in using real world behaviors/ actions and expressions to drive effects


The process of creating an AR garment is largely dependent on the target platform.

Some of them include: 
  - Lens Studio (Snapchat)
  - Effect house(Tik Tok)
  - Meta Spark (Instagram)
  - Web AR
  - Vuforia
  - Unity AR

Here we explore creating for the social AR platforms- snapchat since it allows for full body tracking and people have easy access to it without downloading a separate standalone app.

Here are some examples of AR Lenses we’ve created:

<img src="https://user-images.githubusercontent.com/122074866/236392067-b02e0c00-093b-49e7-a1d1-f1f84151c3fa.gif" height=350/><img src="https://user-images.githubusercontent.com/122074866/235943537-021b382b-5995-4e16-a556-47d8c6fe9cf5.gif" height=350/>

## 3d Creation process (Lens Studio- snapchat)
## There are 2 ways in going about this-

  - Using lens studios auto fitting method
  - Rigging the garment and matching it with the body tracking component in snapchat.

In our experience the first method only works well with 1 mesh. It fails in scenarios where there is layering (For example skirt over shorts).
We mostly prefer rigging the garment since we have more control towards how it moves in Lens studio.

## Mesh creation and prep 

<img src="https://user-images.githubusercontent.com/122074866/235944907-68d3267c-8182-4588-b3f6-09cb16632deb.png"/>

The 3d creation process starts with the creation of the 3d asset in Clo3d/ Marvelous designer.

It is then taken into blender/ any 3d software for retopology and optimization. For AR it is best to stay under 10k poly count

<img src="https://user-images.githubusercontent.com/122074866/235945231-0fe4ed17-153f-4e31-a953-53c6cd51a938.png"/>

Once the asset is created, we need to rig it using the simple [mixamo rig](https://www.mixamo.com/#/) (mixamo rig is compatible with Lens studio)

<div align="center">
  <img src="https://user-images.githubusercontent.com/122074866/235945279-11d7b834-a465-4e4f-baeb-b9d43c2a35c1.gif"/>
</div>

## Posing:
For snapchat, it’s best to pose around the given mannequin body size so the garment fits proportionally with the [occluders](https://docs.snap.com/lens-studio/references/guides/lens-features/graphics/materials/occluders#introduction) set up later.

<div align="center">
  <img src="https://user-images.githubusercontent.com/122074866/235944977-94a7467b-bcae-485f-8e6a-810c94f8e538.png"/>
</div>

We need to align the bones to match the placement of the base mesh. And then we need to sculpt the garment mesh so that it doesn’t clip into the [Base mesh](https://docs.snap.com/lens-studio/references/guides/lens-features/tracking/body/preparing-external-mesh#preparing-the-mesh).

<div align="center">
  <img src="https://user-images.githubusercontent.com/122074866/235945319-c444d8e7-173d-43b4-b4f0-25f1e6ef9985.gif"/>
</div>
  
The occluder base mesh can be edited a little depending on what areas the garment covers. 
(for example the torso is covered by clothing so it doesn't make sense to add occluder underneath it.)

<div align="center">
  <img src="https://user-images.githubusercontent.com/122074866/236392205-c9108438-a3e3-4b01-b7fe-77d9049930cc.png"/>
</div>


After this the file can be exported as an FBX or a Gltf/ Glb since these formats work well for lens studio
[Check out the exporting guide here](https://docs.snap.com/lens-studio/references/guides/adding-content/3d/exporting-content/overview#introduction)

## Lens studio
After it’s successfully exported, we can import it into Lens studio to set up the Lens.

<img src="https://user-images.githubusercontent.com/122074866/236392094-6026f49d-53a3-4a7e-8af2-675af70fc2a5.png"/>

## Tracking
Rig matching in lens studio (easily compatible with the mixamo rig).
After placing the model in the body tracking component in the scene hierarchy and resizing the object scale, we can easily match the rig to the body tracking asset.-- It will then track the body and move well with our joints

<div align="center">
  <img src="https://user-images.githubusercontent.com/122074866/236392036-35e2a1ac-6fda-4a69-9567-3d2d30e08c5a.png"/>
</div>

## Occluder set up

AR is usually a layer on top of the camera feed. In order for clothes to look realistic- we need to render the camera feed according to certain holes (like arm holes) in the mesh so that the back area is hidden. This is done through occluders.
[Read more here](https://docs.snap.com/lens-studio/references/guides/lens-features/graphics/materials/occluders#introduction)

The areas highlighted in blue are the occluders

<div align="center">
  <img src="https://user-images.githubusercontent.com/122074866/236392181-bbfbf749-045b-40bc-849b-d7a9873cfcbd.png"/>
</div>

## Materials
Some of the unique features in lens studio are the endless possibilities with shader manipulations. 
Here we’ve created a scroll effect for the text on the skirt area using material nodes and logic

<img src="https://user-images.githubusercontent.com/122074866/236392194-db7e9793-45b9-4f0d-a88f-6d8014119228.png"/>

## Final output

<div align="center">
  <img src="https://user-images.githubusercontent.com/122074866/236392268-804dbbcd-2678-4349-a1c8-1c88403ff0eb.gif"/>
</div>

<div align="center">  
  <img src="https://user-images.githubusercontent.com/122074866/236396402-89b3b566-c9f9-47e9-9982-45a184dc3ecb.gif"/>
</div>

## Other possible Enhancements

<img src="https://user-images.githubusercontent.com/122074866/236392093-2fe2d394-09b0-453e-ad41-3fe0237f5452.png"/>

AR tools offer a wide level of customizability and creativity to create robust experiences.
Apart from the material editing capabilities discussed above, Lens studio also offers VFX adding capabilities and can also be explored further.
For example: Below we’ve added starry particles to flora flamboyance for the glamor feel

<div align="center">
  <img src="https://user-images.githubusercontent.com/122074866/236392028-457267a6-35a2-40d5-98cd-ce179d365e98.gif"/>
</div>

Another way of adding magic to a lens experience is by having custom interactions as triggers for certain effects 
For example below we’ve used a pose detection method to trigger a boom effect for cosmic boom

<div align="center">
  <img src="https://user-images.githubusercontent.com/122074866/236392096-4c6b69b9-d135-4cfc-be21-7959994a9f63.gif"/>
</div>


## Resources

[Documentation for Lens studio](https://docs.snap.com/lens-studio/home)

[Mesh optimization](https://sites.stat.washington.edu/wxs/Siggraph-93/siggraph93.pdf)

[Mixamo for rigging](https://www.mixamo.com/#/)

