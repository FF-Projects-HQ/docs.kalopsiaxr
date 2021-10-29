---
title: Supported Extensions
parent: Before Import
grand_parent: Maintenance Editor
has_children: true
nav_order: 2
---

**Supported Extensions**\
Our editor and VR client use **GLTF/GLB** extension family to operate.\
But our software can convert **IGES and STEP** files to proper GLB files to work with them.\
So, just export your model from your CAD program with IGES or STEP extensions. Editor will handle the rest.

**Discovered Extension Issues**\
These issues are not related with our ecosystem. These are extensions' and CAD programs' limitations.
+ FBX and OBJ files which exported directly from Autodesk Inventor and/or Solidworks can not support Assembly/Sub-Assembly/Part hierarchy and component names.
+ STL extension simply merges all object to create one object. So, you can not touch a specific inferior object from assembly (like a bolt)
+ Parasolid extensions (both binary and text) can support hierarchy but does not contain component/part names when exported from Autodesk Inventor as we exprienced.
+ IAM and Solidworks files are avaible only with additional licenses so we did not want to increase cost of our programs.

**Suggested Converters**
+ We integrated OpenCASCADE pyOCT based converter technology to our editor. So you can convert your models with it without additional software installation.
+ Babylon JS plugin for 3Ds Max has perfect GLTF support. You can use it and plugin is free. Also you can see component names and hierarchy before export. But you need Autodesk 3Ds Max License.
+ OpenCASCADE CAD Assistant has perfect GLTF support. You can use it and it's completely free. Also you can see component names and hierarchy before export.

**Warnings About GLTF/GLB Extensions**
+ IGES and STEP files have best conversion results according to our test results.
+ We DO NOT suggest to use Solidworks Visualize for GLB export. Because it exports all surfaces as a static mesh component. For this reason if you want to touch a bolt, you will have two object. First one is its head and second one is its body.
+ GLB files use JSON based structure. So lots of companies create their GLTF variants. We use Khronos Group's original GLTF structure and Draco compression. For this reason, we don't suggest converters other than mentioned above. So, use it others with cautions.
+ We didn't include paid applications and applications which can not import CAD files other than STL (such as Blender, CAD Exchanger and PiXYZ)

**Why We Support Few Formats**
+ We know that some of our competitors supports more extensions from us. In real word scenarios of digital twin usages, engineers works with assemblies which have thousand of components rather than some polished models from 3D markets. Also they need its hierarchy and part names rather than simply looking its shape.
+ Users should have version control and contents will be delivered to clients from a center to prevent unnecessary duplications and version conflictings. GLTF format specifically created for this purpose. Because a productive and proper simulation solution should keep up with changes in its plant without thinking if it's too much or not. 
+ VR technology is fantastic for personal training but it can not be used on active cases in field. At that point, we suggest our mobile client to our customers. For this reason, 3D contents should support crossplatform features. 
+ We don't want to direct our customers to extensive model preparation stages (especially vendor side ones) for just scenario creation.

**Future Releases**\
We work on Datasmith Runtime Support, right now. But it requires some additional CAD file compability tests and we need to build an API to mobile support before release. So, it will take sometimes. 
