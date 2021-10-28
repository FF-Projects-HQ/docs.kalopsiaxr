---
title: What Is Not Kalopsia XR ?
parent: About
has_children: true
nav_order: 2
---

It is a fact that Kalopsia XR has advance graphics features thanks to its Unreal Engine 4, Nvidia RTXGI and DLSS based structure.

But it is not a product visualization or marketing focused "render engine" such as VRAY, Autodesk Arnold, Autodesk VRED, Marmoset Toolbag and Keyshot.

For this reason, it has not these features
* Shadows
* Material Creation Editor

Let's have a detailed explaination.

If we integarted an advance material creation editor (for example allowing its user to define PBR texture passes such as normal, metallic, roughness and etc.) we would increase it's learning curve. Also we noticed that maintenance engineers who will build simulations, simply focus on scenario creation and document attachment functions. They dont spend time to create materials.

Simulation contents which created with this editor will be used mainly by "blue-collar stuff" and we noticed that these target users dont notice shadows at all in VR. So disabled this features for gaining extra performance.

But we enabled RTXGI and Ray Traced Reflections because that blue-collar stuffs noticed reflections to give objects some metallic looks.

Even if we disabled these features, we have prepared their functions in our source code. So if our customers will want these features from us, we can just integrate them in a short time.
