---
title: What Is Not Kalopsia XR ?
parent: About
has_children: true
nav_order: 2
---

It is a fact that Kalopsia XR has advance graphics features thanks to its **Unreal Engine 4, Nvidia RTXGI and DLSS** based structure.

But it is not a **product visualization or marketing focused "render engine"** such as VRAY, Autodesk Arnold, Autodesk VRED, Marmoset Toolbag or Keyshot.

**For this reason, we deprecated these features.**
* Shadows
* Material Creation Editor (Material means visualized patterns of objects. For example, rust and/or roughness patterns can be considered as metal materials for objects)

**Let's have a detailed explaination.**

If we integarted an advance material creation editor (for example allowing its user to define PBR texture passes such as normal, metallic, roughness and etc.) we would increase it's learning curve. Also we noticed that maintenance engineers who will build simulations, simply focus on scenario creation and document attachment functions. They dont spend time to create materials. If they want realistic materials, they can define them in Solidworks, Autodesk Inventor or 3Ds Max while drawing their models. All these softwares support PBR and KHR compatible material define functions in their latest versions.

Simulation contents which created with this editor will be used mainly by **"blue-collar stuff"** and we noticed that these target users dont notice shadows at all in VR. So we disabled this feature for gaining extra performance.

**In the other hand, we have these graphics features**
* We enabled **RTXGI and Ray Traced Reflections** because that blue-collar stuffs noticed reflections to give objects some metallic looks.
* We integrated **photography snapshot function** to for enabling its user to get some realistic state photos.
* We integrated **pre-defined material assignment** editor. Engineer can not create a material from start but they can assign various materials from our library to their objects.

**Even if we disabled these features, we prepared their functions in our source code. So if our customers will want these features from us, we can just integrate them in a short time.**
