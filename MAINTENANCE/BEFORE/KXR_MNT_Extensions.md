---
title: Supported Extensions
parent: Before Import
grand_parent: Maintenance Editor
has_children: true
nav_order: 2
---

**Supported Extensions**
Our editor and VR client use **GLTF/GLB** extension to family to operate. But our software can convert IGES and STEP files to proper GLB files to work with them.

+ FBX and OBJ files which exported directly from Autodesk Inventor and/or Solidworks can not support Assembly/Sub-Assembly/Part hierarchy and component names.
+ STL extension simply merges all object to create one object. So, you can not touch a specific inferior object from assembly (like a bolt)
+ Parasolid extensions (both binary and text) can support hierarchy but does not contain component/part names when exported from Autodesk Inventor as we exprienced.
+ IAM and Solidworks files are avaible only with additional licenses so we did not want to increase cost of our programs.

**Suggested Converters**
+ We integrated OpenCASCADE pyOCT based converter technology to our editor. So you can convert your models with it without additional software installation.
+ Babylon JS plugin for 3Ds Max has perfect GLTF support. You can use it and it's free. Also you can see component names and hierarchy before export.
+ OpenCASCADE CAD Assistant has perfect GLTF support. You can use it and it's free. Also you can see component names and hierarchy before export.

**Warnings About GLTF/GLB Extensions**
+ IGES and STEP files have best conversion results according to our test results.
+ We DO NOT suggest to use Solidworks Visualize for GLB export. Because it exports all surfaces as a static mesh component. For this reason if you want to touch a bolt, you will have two object. First one is its head and second one is its body.
+ GLB files uses JSON based structure. So lots of company creates their GLTF variants. We use Khronos Group's original GLTF structure. For this reason, we dont suggest converters other than mentioned above. So, use it others with cautions.

**Why Support Few Formats**
We know that some of our competitors supports more extensions from us. For aspect of digital twin usages in real world, engineers works with assemblies which have thousand of components. Not just some polished models from GrabCAD.
Also simply looking of that models is just meaningless for training purpose. So, 3D model should have same hierarchy structure and names from CAD program.
In the other hand, we dont want to direct our customers to extensive model preparation stages (especially vendor side ones) for just scenario creation.

**Future Releases**
We will work on Datasmith Runtime Support. But it requires some tests and we need to build an API to mobile support. So, it will take sometimes. 
