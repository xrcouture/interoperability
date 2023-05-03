## Creating AR Wearables with snapchat


## Intro

We’ve been developing various games and metaverses. But with AR the ways of creating and experiencing are slightly different.
It’s an interface that we see through the camera. So the possibilities in AR are very much tied to the hardware that is commonly available for users to experience , as well as what the camera and sensors can see. 


Current technologies have come far with ML models working in the backend to allow for human body tracking just through detection from the camera feed! 

Interactions in AR also play very differently as compared to games.Since the camera sees the real world, there are a lot of opportunities in using real world behaviors/ actions and expressions to drive effects


The process of creating an AR garment is largely dependent on the target platform.
  - Some of them include: 
  - Lens Studio (Snapchat)
  - Effect house(Tik Tok)
  - Meta Spark (Instagram)
  - Web AR
  - Vuforia
  - Unity AR

Here we explore creating for the social AR platforms- snapchat since it allows for full body tracking and people have easy access to it without downloading a separate standalone app.

Here are some examples of AR Lenses we’ve created:

<img src="https://user-images.githubusercontent.com/122074866/235943537-021b382b-5995-4e16-a556-47d8c6fe9cf5.gif"/>

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

Once the asset is created, we need to rig it using the simple [mixamo rig](https://) (mixamo rig is compatible with Lens studio)

<img src="https://user-images.githubusercontent.com/122074866/235945279-11d7b834-a465-4e4f-baeb-b9d43c2a35c1.gif"/>

## Posing:
For snapchat, it’s best to pose around the given mannequin body size so the garment fits proportionally with the [occluders](https://) set up later.

<img src="https://user-images.githubusercontent.com/122074866/235944977-94a7467b-bcae-485f-8e6a-810c94f8e538.png"/>

We need to align the bones to match the placement of the base mesh. And then we need to sculpt the garment mesh so that it doesn’t clip into the [Base mesh](https://).

<img src="https://user-images.githubusercontent.com/122074866/235945319-c444d8e7-173d-43b4-b4f0-25f1e6ef9985.gif"/>
The occluder base mesh can be edited a little depending on what areas the garment covers. 
(for example the torso is covered by clothing so it doesn't make sense to add occluder underneath it.)


After this the file can be exported as an FBX or a Gltf/ Glb since these formats work well for lens studio
Check out the exporting guide here

Lens studio
After it’s successfully exported, we can import it into Lens studio to set up the Lens.



Tracking
Rig matching in lens studio (easily compatible with the mixamo rig).
After placing the model in the body tracking component in the scene hierarchy and resizing the object scale, we can easily match the rig to the body tracking asset.-- It will then track the body and move well with our joints



Occluder set up

AR is usually a layer on top of the camera feed. In order for clothes to look realistic- we need to render the camera feed according to certain holes (like arm holes) in the mesh so that the back area is hidden. This is done through occluders.
Read more here
The areas highlighted in blue are the occluders


Materials
Some of the unique features in lens studio are the endless possibilities with shader manipulations. 
Here we’ve created a scroll effect for the text on the skirt area using material nodes and logic



Final output


Other possible Enhancements


AR tools offer a wide level of customizability and creativity to create robust experiences.
Apart from the material editing capabilities discussed above, Lens studio also offers VFX adding capabilities and can also be explored further.
For example: Below we’ve added starry particles to flora flamboyance for the glamor feel



Another way of adding magic to a lens experience is by having custom interactions as triggers for certain effects 
For example below we’ve used a pose detection method to trigger a boom effect for cosmic boom






Resources

Documentation for Lens studio

Mesh optimization

Mixamo for rigging-

