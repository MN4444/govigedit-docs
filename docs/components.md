# Toolset Overview

## Spawn Postions (Required)

These will tell the game where to spawn the Giant and Warrior respectively.

## Killzone (Required)

This is a box that can be adjusted to fit the size of your map, and is required to not allow for the Warrior to simply run off, as well as to destroy objects as to help with performance. Otherwise, objects will be eternally falling, causing perfomance issues over time.

## Map Settings Component (Required)

This is used for configuring data about your map. For example, map name, author, description and preview image.

## Impactable Component

This component will allow the Giant to fissure and shockwave any object it is put on. Highly recommended you put this on all your terrain.

## Ditherable Surface Component

This component will apply a see through effect to any object its applied to.

!> Only works if the material applied is using a dither shader, e.g. GridGrass.

## Giant Boundary

Place this on a GameObject at 0,0,0 and you can use the array system found under the component on the right side (when object is selected) to create points and to adjust your boundary to your liking. An example of what the guardian boundary looks like is found in ExampleMap and Kairos.

## Davigo Network Rigidbody

Add this component to any rigidbody in order to sync it over the network. Required for all rigidbodies.

## Multi Audio Source

This can be added to any object to play sounds to each player, as long as you attach an audio file. Meant to replace the normal Unity AudioSource as it will play for both the Giant and the Warrior.

## Damageable Object

Place this on any object you would like to be able to take damage. Recommended to use alongside the Destructible Object Component. An example can be found on the Rock.

## Destructible Object

Place this component on any object you wish to be able to be destroyed. If Damageable Object is present, this will trigger when it’s health reaches zero. Has many options for customisation. An example can be found on the Rock.

## Rigidbody Explosion

This will be triggered either when Destructible Object is triggered and it has Detonate On Death checked, or if Detonate On Spawn is checked. You can also adjust the impact force required to explode the object so that it does not explode too easily.

## Physics Material

This changes the footstep audio and collision sounds to whatever ScriptableObject is put into Data. Grass and Rock are included by default. To create your own, right click somewhere in the project window, and go to `Create/Physics/Physics Material Data` and assign your own footstep sounds and collision sounds.

## Collision Effector

Add this to objects that should make collision sounds. Make sure the object has a Physics Material (see above) and the Physics Material Data has collision sounds added!
