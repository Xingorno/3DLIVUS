<!-- <html> -->
<!-- <head> -->
<style>
body {
  background-color: #000;
  color: #eee;
}
a { color: #00bfff; }
</style>
<!-- </head> -->
<!-- </html> -->


<div align="center">
  <h1>3DLIVUS: 3D LIVer UltraSound</h1>

<a href="https://www.robarts.ca/peterslab/" target="_blank" rel="noopener noreferrer">
  Fenster Lab, Robarts Research Institute, Western University
</a>
<br>
<a href="https://www.robarts.ca/peterslab/" target="_blank" rel="noopener noreferrer">
  VASST Lab, Robarts Research Institute, Western University
</a>

</div>

## Introudction
This project aims to investigate how 3D ultrasound can improve and facilitate percutaneous thermal liver tumour ablations. It also shows the potentials to translate to other clinical oncological applications, such as renal tumour ablation.

<p align="left">
  <img src="https://img.shields.io/badge/Related work:-red" alt="Related links">
<a href="https://www.ctvnews.ca/london/article/new-robotic-3d-ultrasound-could-improve-liver-cancer-treatment-researchers/" target="_blank" rel="noopener noreferrer">
  <img src="https://img.shields.io/badge/Link1-CTV news-green" alt="Link1">
</a>

<a href="https://www.schulich.uwo.ca/about/news/2023/january/lawson_3d_ultrasound.html" target="_blank" rel="noopener noreferrer">
  <img src="https://img.shields.io/badge/Link2-Schulich School of Medicine & Dentistry-green" alt="Link2">
</a>
</p>

<!-- <p align="center">
  <a href="https://www.youtube.com/watch?v=rgaihhQIr80" target="_blank" rel="noopener noreferrer">
    <img src="figs/3DLIVUS_CTV_demonstration_Cool.png" 
         alt="CTV News - 3DLIVUS Demonstration" 
         width="80%">
  </a>
  <br>
  <em>🎬 Watch the 3DLIVUS system demonstration featured on CTV News (Jan 27, 2023).</em>
</p> -->

<!-- <p align="center">
  <a href="https://youtu.be/hxs5y-deY70" target="_blank" rel="noopener noreferrer">
    <img src="figs/3DLIVUS_demonstration_Cool.png" 
         alt="CTV News - 3DLIVUS Demonstration" 
         width="80%">
  </a>
  <br>
  <em>🎬 Watch the 3DLIVUS system demonstration featured on Schulich School of Medicine & Medicine (Jan., 2023).</em>
</p> -->

<table align="center">
  <tr>
    <td align="center" width="50%">
      <a href="https://www.youtube.com/watch?v=rgaihhQIr80" target="_blank" rel="noopener noreferrer">
        <img src="figs/3DLIVUS_CTV_demonstration_Cool.png" 
             alt="CTV News - 3DLIVUS Demonstration" 
             width="90%">
      </a>
      <br>
      <em>🎬 3DLIVUS featured on CTV News (Jan 27, 2023)</em>
    </td>
    <td align="center" width="50%">
      <a href="https://youtu.be/hxs5y-deY70" target="_blank" rel="noopener noreferrer">
        <img src="figs/3DLIVUS_demonstration_Cool.png" 
             alt="Schulich School - 3DLIVUS Demonstration" 
             width="90%">
      </a>
      <br>
      <em>🎬 Demonstration by Schulich School of Medicine & Dentistry </em>
    </td>
  </tr>
</table>


## Project 1: 3DLIVUS System

<p align="left">
  <img src="https://img.shields.io/badge/Related work:-red" alt="Related work">
  <a href="https://github.com/Xingorno/Robotic-arm-calibration-method-from-scratch">
    <img src="https://img.shields.io/badge/Calibration-Robotic_Arm-green" alt="Arm Calibration">
  </a>
</p>

<p align="justify">
The <strong>3DLIVUS</strong> system integrates <strong>a counterbalanced arm</strong> with encoders and electromechanical locks, <strong>a motor-driven 3D US scanner</strong> mounted at the arm end, and <strong>a workstation</strong> with customized software. It interfaces with any commercial US machine and uses joint encoders in the mechatronic arm for pose tracking, eliminating susceptibility to clinical environmental factors. Operating passively, it allows users to freely maneuver the US transducer while also supporting automated motion along predefined trajectories—60° tilting around the X-axis, 60 mm translation along the Z-axis, and rotation–translation hybrid.
</p>

<p align="justify">
<em>Note: the architecture of our robotic/mechatronic arm is apparently different from the widely used industrial arm, such as <a href="https://www.kuka.com/en-ca/products/robotics-systems/industrial-robots/lbr-iiwa" target="_blank" rel="noopener noreferrer"><strong>LBR iiwa, KUKA</strong></a>. We designed this arm on purpose, which is to better accommodate with liver tumour ablation procedures. For instance, the 3DLIVUS might need to be placed on the opposite side of the patient liver. In this setting, the arm should be long enough to easily reach to the target without bothering the standard workflow. Using the commerically available robot is challenging to adapt this environment.</em>
</p>


<div align="center">
  <img src="figs/3DLIVUS system.png" alt="3DLIVUS system" width="80%">
  <br>
  <em>Figure 1. (a) Overview of the 3DLIVUS system; (b) 3D US scanning mode.</em>
</div>

<br>
<p align="justify">
For the development of 3DLIVUS system, not only the hardware design and maching, such as the counterbalanced arm and 3D US scanner, we have also developed a robust and efficient arm calibration approach. The detailed work can be accessed through the shared badge link.  
</p>


## Project 2: 3D US Acquisition & Clinical Trial
### How does 3DLIVUS acquire images during the procedure?

<p align="justify">
  The 3D US acquisition is fully automatic. During procedure, the physician/sonographer firstly needs to place the convential US probe on the target area of the patient, then the probe can be automatically driven by the 3D US scanner to acquire a sequence of 2D US images, which is used for 3D US reconstruction. The whole process (including reconstruction) takes around 7-12 seconds.
</p>

<p align="center">
  <a href="https://youtu.be/NFdtQTTbtVk" target="_blank" rel="noopener noreferrer">
    <img src="figs/3DUS_acqui.png" 
         alt="3DLIVUS image acquisition" 
         width="80%">
  </a>
  <br>
  <em>🎬 Watch the 3DLIVUS system demonstration on image acquisition.</em>
</p>

### Patient trial at Victoria Hospital (London, Ontario, Canada)

<div align="center">
  <img src="figs/patient_3DUS.png" alt="3D US" width="80%">
</div>

<br>
<p align="left">
  This figure shows the acquired patient's 3D US images, demonstrating the 3DLIVUS system in action. The related structures, including hepatic vessels, kidney, gallbladder and tumour, and inserted needles can be well captured and visualized in our 3D US images. This achievement served as the critical foundation for investigating the downstream tasks related to percutaneous liver tumour ablation, including intra-procedural tumour coverage assessment, improving tumour identification and needle tracking, please see details in below.
</p>

## Project 3: Intra-procedural Tumour Coverage Assessment
<p align="left">
<a href="https://github.com/Xingorno/3DUS-Based-Tumor-Coverage-Evaluation-And-Optimization"><img src="https://img.shields.io/badge/Related work:-red" alt="Project Page"></a>

<a href="https://github.com/Xingorno/3DUS-Based-Tumor-Coverage-Evaluation-And-Optimization" target="_blank" rel= "noopener noreferrer">
  <img src="https://img.shields.io/badge/Topic 1-Tumour Coverage Evaulation and Optimization in 3D US images-green" alt="Tumour coverage evaluation" >
</a>

<a href="https://www.ovid.com/journals/medph/abstract/00005706-202208000-00083~tumour-coverage-evaluation-for-percutaneous-liver-tumour" target="_blank" rel= "noopener noreferrer">
  <img src="https://img.shields.io/badge/Topic 2-2D US vs. 3D US-green" alt="Tumour coverage evaluation" >
</a>
</p>



## Project 4: Tumour Identification
<p align="left">
<a href=""><img src="https://img.shields.io/badge/Related work:-red" alt="Project Page"></a>

<a href="https://github.com/Xingorno/3DUS-CT-or-MRI-Rigid-Registration" target="_blank" rel= "noopener noreferrer">
  <img src="https://img.shields.io/badge/Topic 1-3D&nbsp;US&ndash;to&ndash;CT/MRI registration-green" alt="3D US-CT/MRI registration" >
</a>

<a href="https://github.com/Xingorno/DeepRegS2V" target="_blank" rel= "noopener noreferrer">
  <img src="https://img.shields.io/badge/Topic 2-2D&ndash;to&ndash;3D US registration-green" alt="2D-to-3D registration" >
</a>

<a href="https://github.com/Xingorno/TPS-based-Interactive-Deformable-Registration" target="_blank" rel= "noopener noreferrer">
  <img src="https://img.shields.io/badge/Topic 3-Interactive deformable registration-green" alt="Interactive deformable registration" >
</a>


</p>

## Project 5: Needle Identification (Ongoing...)
