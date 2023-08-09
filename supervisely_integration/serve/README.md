<div align="center" markdown>
<img src="https://github.com/supervisely-ecosystem/serve-segment-anything-hq/assets/115161827/b84249b6-17f3-42f4-ad16-4a6aca2aae4a"/>  

# Serve Segment Anything in High Quality
  
<p align="center">
  <a href="#Overview">Overview</a> •
  <a href="#How-to-Run">How to Run</a> •
  <a href="#Model-application-examples">Model application examples</a> •
  <a href="#Controls">Controls</a> •
  <a href="#Acknowledgment">Acknowledgment</a> 
</p>

[![](https://img.shields.io/badge/supervisely-ecosystem-brightgreen)](https://ecosystem.supervise.ly/apps/supervisely-ecosystem/serve-segment-anything-hq/supervisely_integration/serve)
[![](https://img.shields.io/badge/slack-chat-green.svg?logo=slack)](https://supervise.ly/slack)
![GitHub release (latest SemVer)](https://img.shields.io/github/v/release/supervisely-ecosystem/serve-segment-anything-hq/supervisely_integration/serve)
[![views](https://app.supervise.ly/img/badges/views/supervisely-ecosystem/serve-segment-anything-hq/supervisely_integration/serve.png)](https://supervise.ly)
[![runs](https://app.supervise.ly/img/badges/runs/supervisely-ecosystem/serve-segment-anything-hq/supervisely_integration/serve.png)](https://supervise.ly)
 
</div>

# Overview

🔥 Try HQ-SAM to upgrade [SAM](https://app.supervisely.com/ecosystem/apps/serve-segment-anything-model?id=246) for high-quality zero-shot segmentation. Refer to this [paper](https://arxiv.org/abs/2306.01567) for more details.

[Citation](https://github.com/SysCV/sam-hq/tree/main): *"The recent Segment Anything Model (SAM) represents a big leap in scaling up segmentation models, allowing for powerful zero-shot capabilities and flexible prompting. Despite being trained with 1.1 billion masks, SAM's mask prediction quality falls short in many cases, particularly when dealing with objects that have intricate structures. We propose HQ-SAM, equipping SAM with the ability to accurately segment any object, while maintaining SAM's original promptable design, efficiency, and zero-shot generalizability. Our careful design reuses and preserves the pre-trained model weights of SAM, while only introducing minimal additional parameters and computation."*

Visual comparison between SAM and HQ-SAM
-----------------
**SAM vs. HQ-SAM**
<table>
  <tr>
    <td><img src="https://github.com/supervisely-ecosystem/serve-segment-anything-hq/assets/119248312/0c8fb97d-589c-4b8e-89b3-83964187bf06" width="250"></td>
    <td><img src="https://github.com/supervisely-ecosystem/serve-segment-anything-hq/assets/119248312/e73c2c7d-e06c-4279-b698-039609b492bb" width="250"></td>
    <td><img src="https://github.com/supervisely-ecosystem/serve-segment-anything-hq/assets/119248312/c24c490b-3ab3-4f28-bb89-1351b48b1730" width="250"></td>
  </tr>
  <tr>
    <td><img src="https://github.com/supervisely-ecosystem/serve-segment-anything-hq/assets/119248312/369e372f-4e14-4c7a-bf08-3153cccbf52a" width="250"></td>
    <td><img src="https://github.com/supervisely-ecosystem/serve-segment-anything-hq/assets/119248312/afab550e-d909-4886-b40e-fd28699d73dc" width="250"></td>
    <td><img src="https://github.com/supervisely-ecosystem/serve-segment-anything-hq/assets/119248312/bbd79dcf-74c8-45a3-8b4b-c1b7c8a09dda" width="250"></td>
  </tr>
</table>

<img width="900" alt="image" src='https://github.com/supervisely-ecosystem/serve-segment-anything-hq/assets/119248312/fcdcae25-e4c8-4dab-a6dd-33b216b123ac'>

<br>
</br>

**Application key points:**  
- Manually selected ROI
- Deploy on GPU(faster) or CPU(slower)
- Accurate predictions in most cases
- Correct prediction interactively with `green` and `red` clicks
- Select one of 3 pretrained models
- Models are class agnostic, you can segment any object from any domain


The Segment Anything Model (SAM) can generate masks for objects on images using different types of prompts such as points and bounding boxes, and it can also be applied to raw image to generate masks for all objects.

<p align="center">
<img src="https://user-images.githubusercontent.com/119248312/229991240-9afc6fc9-fc94-45b0-bf96-40d1dda82ba0.jpg" width="950"/>
</p>

Besides segmenting new objects, proposed method allows to correct external masks, e.g. produced by other
instance or semantic segmentation models. A user can fix false negative and false positive regions with positive 🟢
and negative 🔴 clicks, respectively.

🔥🔥🔥 Check out our [youtube tutorial](https://youtu.be/PQCdLCN7uCo) and the [complete guide](https://supervisely.com/blog/xmem-segment-anything-video-object-segmentation/) in our blog:

<a href="https://youtu.be/PQCdLCN7uCo" target="_blank"><img src="https://github.com/supervisely-ecosystem/XMem/assets/106374579/c4c18f53-27f0-4469-8a07-f59404199e64"/></a>


# How to Run

**Pretrained models**

1. Start the application from Ecosystem.

<img src="https://github.com/supervisely-ecosystem/serve-segment-anything-hq/assets/119248312/fd120e1a-bdda-4492-b193-33147f5ba2f0"/> 

2. Select the pretrained model and deploy it on your device by clicking `Serve` button.
<img src="https://user-images.githubusercontent.com/115161827/232102026-99725e52-d844-44fd-8449-061f84116cf6.png" />

3. You'll see `Model has been successfully loaded` message indicating that the application has been successfully started and you can work with it from now on.

<p align="center">
  <img src="https://user-images.githubusercontent.com/115161827/229956389-bb8780db-9bd8-442b-aa28-cfc552316bc5.png" height="140px" />
</p>


**Custom models**

Copy model file path from Team Files and select model architecture:

https://user-images.githubusercontent.com/91027877/232559973-dca553e1-d86f-4808-aaab-cf68bafc0e6f.mp4

# Model application examples

Single-click segmentation of a complicated object using Smart Tool:

https://user-images.githubusercontent.com/91027877/232552579-8f616853-531b-4531-90a1-773e265f9792.mp4

Mask correction with Positive and Negative points in Smart Tool:
  
https://user-images.githubusercontent.com/115161827/232538639-02c688c5-58bd-4500-b9c9-04aa5bf720b0.mp4
  
Applying model in raw mode via NN image labeling app:
  
https://user-images.githubusercontent.com/115161827/232538575-1863ff7a-1f7e-418a-8157-7cdd4364abdc.mp4

Applying model to object in bounding box:
  
https://user-images.githubusercontent.com/115161827/232538528-477a18ad-e701-4d0b-8ce7-6abff3246197.mp4
 
Applying model to the points:

https://user-images.githubusercontent.com/91027877/233379739-8fbfe2d0-7232-40ba-8de1-dc209069edd5.mp4
  
Applying model in the combined mode (using both points and bounding box):
  
https://user-images.githubusercontent.com/115161827/232538470-db1ed291-aa0a-48df-ae83-5e82193aca51.mp4

If you want predicted masks to be automatically overdrawn be replacing old masks with new masks, you can set "replace_masks" parameter to true:

https://user-images.githubusercontent.com/91027877/233377950-c480eb09-4727-41ca-ab8f-24214ed9d945.mp4

You can also use this app for segmenting objects on videos using [video labeling tool](https://ecosystem.supervise.ly/apps/video-labeling-tool) (here is full [guide](https://www.youtube.com/watch?v=eaAh856QKYg) on working with smart tool in video labeling tool):

https://user-images.githubusercontent.com/91027877/233416370-6e37d654-96eb-42fe-91f0-4ea7a6e6503a.mp4

If you want to label batch of images fast, you can use this app in combination with [batched smart tool](https://ecosystem.supervisely.com/apps/dev-smart-tool-batched):

https://user-images.githubusercontent.com/91027877/239091427-cc8cf488-db46-4786-b878-ba71af85f99c.mp4

# Controls

| Key                                                           | Description                               |
| ------------------------------------------------------------- | ------------------------------------------|
| <kbd>Left Mouse Button</kbd>                                  | Place a positive click                    |
| <kbd>Shift + Left Mouse Button</kbd>                          | Place a negative click                    |
| <kbd>Scroll Wheel</kbd>                                       | Zoom an image in and out                  |
| <kbd>Right Mouse Button</kbd> + <br> <kbd>Move Mouse</kbd>    | Move an image                             |
| <kbd>Space</kbd>                                              | Finish the current object mask            |
| <kbd>Shift + H</kbd>                                          | Higlight instances with random colors     |
| <kbd>Ctrl + H</kbd>                                           | Hide all labels                           |


<p align="left"> <img align="center" src="https://i.imgur.com/jxySekj.png" width="50"> <b>—</b> Auto add positivie point to rectangle button (<b>ON</b> by default for SmartTool apps) </p>

<div align="center" markdown>
<img src="https://user-images.githubusercontent.com/119248312/229995019-9a9dece7-516f-4b44-8b73-cdd01c1a4178.jpg" width="90%"/>
</div>

<p align="left"> <img align="center" src="https://user-images.githubusercontent.com/119248312/229998670-21ced133-903f-48ce-babb-e22408d2580c.png" width="150"> <b>—</b> SmartTool selector button, switch between SmartTool apps and models</p>

<div align="center" markdown>
<img src="https://user-images.githubusercontent.com/119248312/229995028-d33b0423-6510-4747-a929-e0e860ccabff.jpg" width="90%"/>
</div>

# Acknowledgment

This app is based on the great work `Segment Anything`: [github](https://github.com/facebookresearch/segment-anything). ![GitHub Org's stars](https://img.shields.io/github/stars/facebookresearch/segment-anything?style=social)
