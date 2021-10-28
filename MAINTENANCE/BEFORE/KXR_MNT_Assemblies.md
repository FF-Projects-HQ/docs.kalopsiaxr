---
title: Assembly Structures
parent: Before Import
grand_parent: Maintenance Editor
has_children: true
nav_order: 1
---

**Why We Use Game Engines ?**\
If we want to create realtime interactive simulation contents with advance realistic graphics for VR platform, we need to use some specific specific frameworks and APIs such as DirectX, Vulkan and OpenXR.\
For this reason even if we dont use branded engines like Unreal Engine or Unity and build our in-house technology, back-end will roughly be same. It will become some kind of a game engine.\
Right now we use Unreal Engine 4 to build our custom simulations and Kalopsia XR ecosystem.

**Understanding of Game Engines**\
3D contents for game engines have different characteristic than CAD files. So, we can not import everything directly without some rules.
+ Main Assembly files (for example a collaborative robot model) is equal to an **Actor Class**
+ Sub-Assemblies (for example gripper group of that collaborative robot) is equal to **Scene Components**. Because they do not have body or mesh. But they works like an empty/ghost volume to become a parent of couple mesh components.
+ Parts (for example a bolt a plate of gripper group of that collaborative robot) is equal to **Static Mesh Components**.\
Also, lots of CAD program features is avaible only for their ecosystem.

**Assembly Hierarchy**\
If you want see proper hierarchy in editor and VR, you need to use **Assembly > Sub-Assembly > Part** workflow rather than just **Motion Study** defination.
So, you can not lay all objects to assembly's root and expect a proper hierarchy.

**Part Structure**\
If you dont need to access inferior objects of group, they should located in part.

For example, you want to create a scenario for removing 5 bolt and you dont want to remove them one by one. They should come all in once.
To achive this, you need add them in a **part** rather than an assembly.

**Performance Suggestions**\
You can visualize potentially thousands of components in Kalopsia XR thanks to its game engine based backend. But you should divide them multiple assemblies.\
For example if you need to visualize a casting plant, you need to create multiple assemblies for oven group, elevator group and etc. Because VR application performance is not all about its rendering performance. It is also about feature mechanics. So, calculating thousand components at once will be very performance consuming and we dont suggest that.
