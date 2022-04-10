# Creating Rigidbody Objects

?> What does this allow? Custom rigidbodies allows for map makers to make their own special throwable objects! Such as a barrel, crate, and pretty much anything you can think of.

## Setting up your rigidbody
To begin making a custom rigidbody, you want to create an empty game object and reset its transform. This will set its location to 0, 0, 0 on your map, to keep everything in line. Feel free to name this whatever you want, as it affects nothing. For this we will simply leave it as GameObject, but if you are making something such as a barrel, it would be best to name it that.

 ![Resetting Transform](_media/transform-reset.png)

 ### Visuals

Now, you will want to add whatever you would like the object to look like as a child of the object, and this can be done by dragging and dropping your object onto the empty game object, in the hierarchy, and resetting the transform of the object. In this case, a cube. 

 ![Drag Object](_media/gameobjectdrag.png)

 ### Required Components

 Once that is complete, we can begin adding our components. Now the components you will need are going to be listed here. These can be added in any order, just make sure you have them all! Otherwise there will be issues with your rigidbody.

 ![List of Components](_media/complist.png)

 ### Interpolation Targets

 If you expand all your components, you may see that your  Davigo Network Rigidbody has no Interpolation Targe. To fix that, we will rename our cube to "art" and remove its collider as that goes on the empty object, otherwise your object will not have world collisions which obviously, is a big issue.

 ![Interp Target](_media/davinetworkrigidbody.png)

?> What is "art"? This is what Fusion uses to allow you to visually see the objects and their location, otherwise, they would just be invisible to everyone.

# Testing your objects

 Once you've gotten all of those steps complete, then you can test your object in the game itself. First, you generally would want to test to see if well, its simply there.  As if it isn't, then you are either missing a component or did not setup your colliders correctly.

?>Why aren't my Bombs, Rockets, or Cannons showing up when I use them? This is caused when your object does not have an Interpolation Target, as Fusion does not know what to do with networked objects. Simply go through and check all your Interpolation Targets and make sure it says "art"