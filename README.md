# Weapon Slash
  
[![Generic badge](https://img.shields.io/badge/Unity-2019.4.31f1-informational.svg)](https://unity3d.com/unity/whats-new/2019.4.31)
[![Generic badge](https://img.shields.io/badge/SDK-AvatarSDK3-informational.svg)](https://vrchat.com/home/download)
[![Generic badge](https://img.shields.io/badge/License-MIT-informational.svg)](https://github.com/VRLabs/Weapon-Slash/blob/main/LICENSE)
[![Generic badge](https://img.shields.io/github/downloads/VRLabs/Weapon-Slash/total?label=Downloads)](https://github.com/VRLabs/Weapon-Slash/releases/latest)

Perform consecutive slashes with motion.

## How it works

A polar-limited [PhysBone](https://docs.vrchat.com/docs/physbones) creates an offset for a [Contact](https://docs.vrchat.com/docs/contacts) system to play animations when a slashing motion is done with your arm. A networking layer animates a separate PhysBone hierarchy to account for "IK Smoothing".

## Preview

https://user-images.githubusercontent.com/45078979/165919653-4f94821d-35aa-4ab8-9812-87bec78197df.mp4

## Install guide

https://user-images.githubusercontent.com/45078979/165899876-4141201a-99ef-4a0c-98af-d849b3da1792.mp4

[Cancerspace shader](https://github.com/AkaiMage/VRC-Cancerspace) is required for the default effect.

Merge the FX controller to your own FX controller, using the [Avatars 3.0 Manager](https://github.com/VRLabs/Avatars-3.0-Manager) tool.

"WeaponSlash.Sync" is a synced parameter, so click the checkbox within the tool to add it to your avatar's parameter asset.
 
"Weapon Slash.prefab" should go to the base of your Unity scene, which will give it base Unity scaling.

Unpack the prefab by right-clicking it.

Place "Weapon Slash" at the base of your avatar.

Locate "Weapon Slash/Weapon". You can replace "Weapon Slash/Weapon/キューブソード" with your own prop. Keep your prop in the same placement and facing the same way as the default prop. Put "Weapon Slash/Weapon" under your avatar's wrist hierarchy(Not the "Weapon Slash/Effects/.../Wrist"). Set the "Weapon" object transforms so the prop appears correctly in your hand.

## How to use

**"WeaponSlash.Control" parameter must be true for the system to be active.**

By default, the gesture for activating the Heavy Slash is _fingerpoint_. This is changeable, but there are a lot of transitions to find. Will eventually have a solution which isn't an extra layer, in the form of a setup script.

Under the "Weapon Slash/Effects/(Light or Heavy) Slash" hierarchy are Containers. Place custom effects within these Containers. "Weapon/(Light or Heavy) Effect Target" is where these effects will appear.

You can edit "Weapon Slash/Dynamics/PhysBone" to change the difficulty of the slash. For further adjustment you can also change the radius of "Weapon Slash/Dynamics/Receiver".

## Downloads

You can grab the latest version of the Weapon Slash in [Releases](https://github.com/VRLabs/Weapon-Slash/releases/latest).

## License

Weapon Slash is available as-is under MIT. For more information see [LICENSE](https://github.com/VRLabs/Weapon-Slash/blob/main/LICENSE).

## Contact us

If you need help, our support channel is on [Discord](https://discord.vrlabs.dev).
