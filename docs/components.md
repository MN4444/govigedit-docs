# Components and Toolset

## Primary Tools

?> What are "primary tools"? These are the main components and prefabs you will be using while creating your maps.

#### Spawn Postions (Required Prefabs)

These will tell the game where to spawn the Giant and Warrior respectively.

#### Killzone (Required Prefab)

This is a box that can be adjusted to fit the size of your map, and is required to not allow for the Warrior to simply run off, as well as to destroy objects as to help with performance. Otherwise, objects will get stuck in places and never dissapear.

#### Map Settings (Required Prefab)

This can be placed anywhere in your map, and is recommended to be filled out prior to export or your map will have no author, name, or description.
#### Impactable

This component will allow the Giant to fissure and shockwave any object it is put on. Highly recommended you put this on all your terrain.

#### Ditherable Surface Component

This component will apply a see through effect to any object its applied to.

!> Only works if the material applied is using Tri Planar Normal, like GridGrass

## Components List

#### Giant Boundary

Place this on an object such as a cube at 0,0,0 and you can use the array system found under the component on the right side (when object is selected) to create points and to adjust your boundary to your liking.

#### Davigo Network Rigidbody

Add this component to any rigidbody (Physics Object) in order to sync it over the network. Required for all rigidbodies.

#### Multi Audio Source

This can be added to any object to play sounds to each player, as long as you attach an audio file. Meant to replace the normal Unity AudioSource as it will play for both the Giant and the Warrior.

#### Damageable Object

Place this on any object you would like to be able to take damage. Recommended to use alongside the Destructible Object Component.

#### Destructible Object

Place this component on any object you wish to be able to be destroyed. If Damageable Object is present, this will trigger when it’s health reaches zero. Has many options for customisation.

#### Rigidbody Explosion

This will be triggered either when Destructible Object is triggered and it has Detonate On Death checked, or if Detonate On Spawn is checked. You can also adjust the impact force required to explode the object so that it does not explode too easily.

#### Physics Material

This changes the footstep audio and collision sounds to whatever ScriptableObject is put into Data. Grass and Rock are included by default. To create your own, right click somewhere in the project window, and go to `Create/Physics/Physics Material Data` and assign your own footstep sounds and collision sounds.

#### Collision Effector

Add this to objects that should make collision sounds. Make sure the object has a Physics Material (see above) and the Physics Material Data has collision sounds added!
