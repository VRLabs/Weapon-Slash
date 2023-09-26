<div align="center">

# Weapon Slash

[![Generic badge](https://img.shields.io/github/downloads/VRLabs/Weapon-Slash/total?label=Downloads)](https://github.com/VRLabs/Weapon-Slash/releases/latest)
[![Generic badge](https://img.shields.io/badge/License-MIT-informational.svg)](https://github.com/VRLabs/Weapon-Slash/blob/main/LICENSE)
[![Generic badge](https://img.shields.io/badge/Unity-2019.4.31f1-lightblue.svg)](https://unity3d.com/unity/whats-new/2019.4.31)
[![Generic badge](https://img.shields.io/badge/SDK-AvatarSDK3-lightblue.svg)](https://vrchat.com/home/download)

[![Generic badge](https://img.shields.io/discord/706913824607043605?color=%237289da&label=DISCORD&logo=Discord&style=for-the-badge)](https://discord.vrlabs.dev/)
[![Generic badge](https://img.shields.io/endpoint.svg?url=https%3A%2F%2Fshieldsio-patreon.vercel.app%2Fapi%3Fusername%3Dvrlabs%26type%3Dpatrons&style=for-the-badge)](https://patreon.vrlabs.dev/)

A movement based weapon effect trigger system

![Alt text]()

### ⬇️ [Download latest Unitypackage](https://github.com/VRLabs/Weapon-Slash/releases/latest)

<!-- 
### 📦 [Add to VRChat Creator Companion]() -->

</div>

---

## How it works

* A polar-limited [PhysBone](https://docs.vrchat.com/docs/physbones) creates an offset for a [Contact](https://docs.vrchat.com/docs/contacts) system to play animations when a slashing motion is done with your arm.
* A networking layer animates a separate PhysBone hierarchy to account for [IK](https://en.wikipedia.org/wiki/Inverse_kinematics) smoothing.

## Install guide


https://github.com/VRLabs/Weapon-Slash/assets/76777936/129c37e9-101d-4a30-854e-00c03a01016c

* Download and import [Cancerspace shader](https://github.com/AkaiMage/VRC-Cancerspace).
* Merge the Animator Controller ``Weapon Slash FX`` to your own FX Controller, using the [Avatars 3.0 Manager](https://github.com/VRLabs/Avatars-3.0-Manager) tool.
* Merge the Expression Parameter List``Weapon Slash Expressions```to your own Expression Parameter List, using the [Avatars 3.0 Manager](https://github.com/VRLabs/Avatars-3.0-Manager) tool.
* Drag & drop the ``Weapon Slash`` prefab into the base of your Hierarchy.
* Right click and unpack the prefab, then drag & drop it onto your avatar.
* Expand the prefab hierarchy and find ``Weapon Slash`` -> ``Weapon``
* Move ``Weapon`` outside of ``Weapon Slash`` and place it on the left or right wrist of your avatar.
  * Adjust the position and rotation of ``Weapon`` to fit into your hand.
  * You can replace ``Weapon`` -> ``キューブソード`` with your own prop. Keep your prop in the same placement and facing the same way as the default prop.

## How to use

* ``WeaponSlash/Control`` parameter must be True for the system to be active.
* ``WeaponSlash/HeavyActive`` parameter must be True for the Heavy Slash to be enabled.
* Under the ``Weapon Slash/Effects/(Light or Heavy) Slash`` hierarchy are Containers. Place custom effects within these Containers. ``Weapon/(Light or Heavy) Effect Target`` is where these effects will appear.
* You can edit ``Weapon Slash/Dynamics/PhysBone`` to change the force required for the slash. For further adjustment you can also change the radius of ``Weapon Slash/Dynamics/Receiver``.

## Performance stats

System:

```c++
Constraints:        12
Contact Receivers:  2
Contact Senders:    2
FX Animator Layers: 4
Parameter Memory:   3 
Phys Bones:         2
```

Default Weapon:

```c++
Material slots:     2
Mesh Renderers:     2
```

Default Effects:

```c++
Audio Sources:      7
Particle Systems:   11
```

## Hierarchy layout

```html
Weapon Slash
|-Dynamics
|  |-PhysBone
|  |-Receiver
|  |-Remote
|  |  |-PhysBone
|  |  |-Receiver
|-Effects
|  |-Light Slash
|  |  |-A
|  |  |  |-Container
|  |  |  |  |-Particle System
|  |  |  |  |-Audio
|  |  |-B
|  |  |  |-Container
|  |  |  |  |-Particle System
|  |  |  |  |-Audio
|  |  |-C
|  |  |  |-Container
|  |  |  |  |-Particle System
|  |  |  |  |-Audio
|  |-Heavy Slash
|  |  |-Weak
|  |  |  |-A
|  |  |  |  |-Container
|  |  |  |  |  |-Particle System
|  |  |  |  |  |  |-Particle System
|  |  |  |  |  |-Audio
|  |  |  |-B
|  |  |  |  |-Container
|  |  |  |  |  |-Particle System
|  |  |  |  |  |  |-Particle System
|  |  |  |  |  |-Audio
|  |  |  |-C
|  |  |  |  |-Container
|  |  |  |  |  |-Particle System
|  |  |  |  |  |  |-Particle System
|  |  |  |  |  |-Audio
|  |  |-Strong
|  |  |  |-Container
|  |  |  |  |-Particle System
|  |  |  |  |  |-Particle System
|  |  |  |  |-Audio
|-Weapon
|  |-キューブソード
|  |  |-Blade
|  |  |-Hilt
|  |-Light Effect Target
|  |-Heavy Effect Target
```

## Contributors

* [lin](https://github.com/oofdesu)

## License

Weapon Slash is available as-is under MIT. For more information see [LICENSE](https://github.com/VRLabs/Weapon-Slash/blob/main/LICENSE).

​

<div align="center">

[<img src="https://github.com/VRLabs/Resources/raw/main/Icons/VRLabs.png" width="50" height="50">](https://vrlabs.dev "VRLabs")
<img src="https://github.com/VRLabs/Resources/raw/main/Icons/Empty.png" width="10">
[<img src="https://github.com/VRLabs/Resources/raw/main/Icons/Discord.png" width="50" height="50">](https://discord.vrlabs.dev/ "VRLabs")
<img src="https://github.com/VRLabs/Resources/raw/main/Icons/Empty.png" width="10">
[<img src="https://github.com/VRLabs/Resources/raw/main/Icons/Patreon.png" width="50" height="50">](https://patreon.vrlabs.dev/ "VRLabs")
<img src="https://github.com/VRLabs/Resources/raw/main/Icons/Empty.png" width="10">
[<img src="https://github.com/VRLabs/Resources/raw/main/Icons/Twitter.png" width="50" height="50">](https://twitter.com/vrlabsdev "VRLabs")

</div>

---
