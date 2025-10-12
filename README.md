
<style>
body,.markdown-body, table, td, tr{
  background-color: #000;
  color: #eee;
}
a { color: #00bfff; }
</style>



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
<p align="left">
  <img src="https://img.shields.io/badge/Related work:-red" alt="Related links">
<a href="https://www.ctvnews.ca/london/article/new-robotic-3d-ultrasound-could-improve-liver-cancer-treatment-researchers/" target="_blank" rel="noopener noreferrer">
  <img src="https://img.shields.io/badge/Link1-CTV news-green" alt="Link1">
</a>

<a href="https://www.schulich.uwo.ca/about/news/2023/january/lawson_3d_ultrasound.html" target="_blank" rel="noopener noreferrer">
  <img src="https://img.shields.io/badge/Link2-Schulich School of Medicine & Dentistry-green" alt="Link2">
</a>
</p>

This project aims to investigate how 3D ultrasound can improve and facilitate percutaneous thermal liver tumour ablations. It also shows the potentials to translate to other clinical oncological applications, such as renal tumour ablation.



<table align="center" border="0" cellspacing="0" cellpadding="0" style="border:none; border-collapse:collapse; border-spacing:0; border-top:0; border-bottom:0;">
  <tr>
    <td align="center" width="50%" style="border:none; padding:0;">
      <a href="https://www.youtube.com/watch?v=rgaihhQIr80" target="_blank" rel="noopener noreferrer">
        <img src="figs/3DLIVUS_CTV_demonstration_Cool.png" 
             alt="CTV News - 3DLIVUS Demonstration" 
             width="90%">
      </a>
      <br>
      <em>🎬 3DLIVUS featured on CTV News (Jan 27, 2023)</em>
    </td>
    <td align="center" width="50%" style="border:none; padding:0;">
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
  <a href="https://github.com/Xingorno/MICCAI2025-2DUS-to-CTMRI-Multimodal-Registration" target="_blank" rel="noopener noreferer">
    <img src="https://img.shields.io/badge/3D US Integration-MICCAI2025 Highlight-green" alt="3D US integration">
  </a>
  <a href="https://github.com/Xingorno/Robotic-arm-calibration-method-from-scratch">
    <img src="https://img.shields.io/badge/Calibration-Robotic_Arm-green" alt="Arm Calibration">
  </a>
</p>

<p align="justify">
The <strong>3DLIVUS</strong> system integrates <strong>a counterbalanced arm</strong> with encoders and electromechanical locks, <strong>a motor-driven 3D US scanner</strong> mounted at the arm end, and <strong>a workstation</strong> with customized software. It interfaces with any commercial US machine and uses joint encoders in the mechatronic arm for pose tracking, eliminating susceptibility to clinical environmental factors. Operating passively, it allows users to freely maneuver the US transducer while also supporting automated motion along predefined trajectories—60° tilting around the X-axis, 60 mm translation along the Z-axis, and rotation–translation hybrid.
</p>

<p align="justify">
<em>Note: the architecture of our robotic/mechatronic arm is apparently different from the widely used industrial arm, such as <a href="https://www.kuka.com/en-ca/products/robotics-systems/industrial-robots/lbr-iiwa" target="_blank" rel="noopener noreferrer">LBR iiwa, KUKA</a>. We designed this arm on purpose, which is to better accommodate with liver tumour ablation procedures. For instance, the 3DLIVUS might need to be placed on the opposite side of the patient liver. In this setting, the arm should be long enough to easily reach to the target without bothering the standard workflow. Using the commerically available robot is challenging to adapt this environment.</em>
</p>


<div align="center">
  <img src="figs/3DLIVUS system.png" alt="3DLIVUS system" width="80%">
  <br>
  <em>Figure 1. (a) Overview of the 3DLIVUS system; (b) 3D US scanning mode.</em>
</div>

<br>
<p align="justify">
For the development of 3DLIVUS system, not only the hardware design and maching, such as the counterbalanced arm and 3D US scanner, we have also developed a robust and efficient arm calibration approach, see the <a href="https://github.com/Xingorno/Robotic-arm-calibration-method-from-scratch" target="_blank" rel="noopener noreferrer">link</a>.  
</p>

<p align="justify">
  Figure 2 shows our proposed framework for integrating 3D US into the standard clinical ablation workflow, which advanced the capabities of 3D US imaging in improving percutaneous tumour ablation, demonstrating the potential to expand the therapeutic role of 3D US in clinical interventions. In detail, the ablation workflow is enhanced with intra-procedural tumour coverage (project 2), tumour identification (project 3), multimodal visualization and instrument tracking (project 4).
</p>
<div align="center">
  <img src="figs/3DLIVUS_intergration_framework_black.png" alt="3DLIVUS frame" width="80%">
  <br>
  <em>Figure 2. Framework for 3D US integration into conventional 2D US guidance. (a) 3DLIVUS system; (b) intra-procedural guidance. Note: the role of 3D US is highlighted in a brown block. (Regi: Registration, Recon: 3D US reconstruction)</em>
</div>

## 3D US Acquisition & Clinical Trial
### How does 3DLIVUS acquire images during the procedure?

<p align="justify">
  The 3D US acquisition is fully automatic. During the procedure, the physician/sonographer first needs to place the conventional US probe on the target area of the patient. Then, the probe can be automatically driven by the 3D US scanner to acquire a sequence of 2D US images, which are used for 3D US reconstruction. The whole process (including reconstruction) takes around 7-12 seconds.
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
  <img src="figs/patient_3DUS_black.png" alt="3D US" width="80%">
</div>

<br>
<p align="left">
  This figure shows the acquired patient's 3D US images, demonstrating the 3DLIVUS system in action. The related structures, including hepatic vessels, kidney, gallbladder and tumour, and inserted needles can be well captured and visualized in our 3D US images. This achievement served as the critical foundation for investigating the downstream tasks related to percutaneous liver tumour ablation, including intra-procedural tumour coverage assessment, improving tumour identification and needle tracking, please see details in below.
</p>

## Project 2: Intra-procedural Tumour Coverage Assessment
<p align="left">
<a href="https://github.com/Xingorno/3DUS-Based-Tumor-Coverage-Evaluation-And-Optimization"><img src="https://img.shields.io/badge/Related work:-red" alt="Project Page"></a>

<a href="https://github.com/Xingorno/3DUS-Based-Tumor-Coverage-Evaluation-And-Optimization" target="_blank" rel= "noopener noreferrer">
  <img src="https://img.shields.io/badge/Tumour Coverage Evaulation and Optimization in 3D US images-IEEE TMI-green" alt="Tumour coverage evaluation" >
</a>

<a href="https://www.ovid.com/journals/medph/abstract/00005706-202208000-00083~tumour-coverage-evaluation-for-percutaneous-liver-tumour" target="_blank" rel= "noopener noreferrer">
  <img src="https://img.shields.io/badge/2D US vs. 3D US-COMP2022-green" alt="Tumour coverage evaluation" >
</a>
</p>

### Why improve intra-procedural tumour coverage assessment?

<p align="justify">
  In conventional US guidance, as shown in the left figure, the physician typically places a few landmarks on the in-plane 2D US image to estimate the required ablation zone size. Even though a 5 or 10 mm safety margin is commonly applied in clinical practice to reduce the risk of residual tumours, this process may still be insufficient to provide complete tumour coverage. In addition, to ensure safety, the physician must carefully examine multiple US views to avoid ablating critical structures, such as the colon, as shown in the right-hand image.
</p>



<table align="center" border="0" cellspacing="0" cellpadding="0" style="border:none; border-collapse:collapse; border-spacing:0; border-top:0; border-bottom:0;">
  <tr>
    <td align="center" width="40%" style="border:none; padding:0;">
        <img src="figs/Assessment_1.png" 
             alt="Assessment 1" 
             width="90%">
      <!-- <br> -->
      <em>Tumour coverage assessment on 2D US</em>
    </td>
    <td align="center" width="40%" style="border:none; padding:0;">
        <img src="figs/Assessment_2.png" 
             alt="Assessment 2" 
             width="95%">
      <!-- <br> -->
      <em>Tumour coverage assessment with surrounding structures </em>
    </td>
  </tr>
</table>

### 3D US-based Tumour Coverage Evaluation

<div align="center">
  <img src="figs/Tumour_coverage_compare.png" alt="3DLIVUS assessment" width="80%">
  <br>
  <em>Figure 3. Comparison of tumour coverage evaluation on 2D and 3D US.</em>
</div>



### 3D US-based Needle Adjustment (If required)



## Project 3: Tumour Identification
<p align="left">
<a href=""><img src="https://img.shields.io/badge/Related work:-red" alt="Project Page"></a>

<a href="https://github.com/Xingorno/3DUS-CT-or-MRI-Rigid-Registration" target="_blank" rel= "noopener noreferrer">
  <img src="https://img.shields.io/badge/3D&nbsp;US&ndash;to&ndash;CT/MRI registration-IPCAI2023-green" alt="3D US-CT/MRI registration" >
</a>

<a href="https://github.com/Xingorno/DeepRegS2V" target="_blank" rel= "noopener noreferrer">
  <img src="https://img.shields.io/badge/2D&ndash;to&ndash;3D US registration-MICCAI&ndash;AECAI2024-green" alt="2D-to-3D registration" >
</a>

<a href="https://github.com/Xingorno/TPS-based-Interactive-Deformable-Registration" target="_blank" rel= "noopener noreferrer">
  <img src="https://img.shields.io/badge/Interactive deformable registration-3D Slicer Extension-green" alt="Interactive deformable registration" >
</a>

</p>

### Why improve tumour identification?

### Our proposed 2D US-to-CT/MRI registration solution


## Project 4: Needle Identification (Ongoing...)

### Why improve needle tracking?

### What are we doing?
