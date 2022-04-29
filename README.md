# Weapon Slash
  
[![Generic badge](https://img.shields.io/badge/Unity-2019.4.31f1-informational.svg)](https://unity3d.com/unity/whats-new/2019.4.31)
[![Generic badge](https://img.shields.io/badge/SDK-AvatarSDK3-informational.svg)](https://vrchat.com/home/download)
[![Generic badge](https://img.shields.io/badge/License-MIT-informational.svg)](https://github.com/VRLabs/Weapon-Slash/blob/main/LICENSE)
[![Generic badge](https://img.shields.io/github/downloads/VRLabs/Weapon-Slash/total?label=Downloads)](https://github.com/VRLabs/Weapon-Slash/releases/latest)

Perform consecutive slashes with motion.

## How it works

[Contacts](https://docs.vrchat.com/docs/contacts) and a [PhysBone](https://docs.vrchat.com/docs/physbones) cooperate to start animations when a slashing motion is done with your arm.

## Install guide

https://user-images.githubusercontent.com/45078979/165899876-4141201a-99ef-4a0c-98af-d849b3da1792.mp4

Merge the FX controller to your own FX controller, using the [Avatars 3.0 Manager](https://github.com/VRLabs/Avatars-3.0-Manager) tool.

"WeaponSlash.Control" and "WeaponSlash.Sync" are synced parameters, so click their checkboxes within the tool to add them to your avatar's parameter asset. "WeaponSlash.Control" can optionally not be synced if you are otherwise driving it in a synced manner.
 
"Weapon Slash.prefab" should go to the base of your Unity scene, which will give it base Unity scaling.

Unpack the prefab by right-clicking it.

Place "Weapon Slash" at the base of your avatar.

Within the "Weapon Slash/Armature" hierarchy is the "Upper Arm/Lower Arm/Wrist" series of objects. Each of these objects has a parent constraint with "None" in the list of sources. Use the corresponding arm bones within your avatar's humanoid rig to provide a valid source for each constraint.

Locate "Weapon Slash/Weapon". You can replace "Weapon Slash/Weapon/キューブソード" with your own prop. Keep your prop in the same placement and facing the same way as the default prop. Put "Weapon Slash/Weapon" under your avatar's wrist hierarchy(Not the "Weapon Slash/Armature/.../Wrist"). Set the "Weapon" object transforms so the prop appears correctly in your hand.

## How to use

You can edit "Weapon Slash/Armature/Upper Arm/Lower Arm/Wrist/Weapon/PhysBone" to change the difficulty of the slash. For further adjustment you can also change the radius of "Weapon Slash/Armature/Upper Arm/Lower Arm/Wrist/Weapon/Receiver".

Under "Weapon Slash/Armature/(Light or Heavy) Slash" are Containers. Place custom effects within these Containers. "Weapon/(Light or Heavy) Effect Target" is where these effects will appear.

"WeaponSlash.Control" parameter must be true for the system to be active.

By default, the gesture for activating the Heavy Slash is _fingerpoint_. This is changeable, but there are a lot of transitions to find. Will eventually have a solution which isn't an extra layer, in the form of a setup script.

## Downloads

You can grab the latest version of the Weapon Slash in [Releases](https://github.com/VRLabs/Weapon-Slash/releases/latest).

## License

Weapon Slash is available as-is under MIT. For more information see [LICENSE](https://github.com/VRLabs/Weapon-Slash/blob/main/LICENSE).

## Contact us

If you need help, our support channel is on [Discord](https://discord.vrlabs.dev).
