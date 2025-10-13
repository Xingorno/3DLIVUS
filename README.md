
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

<p align="justify">Liver tumour ablation is a minimally invasive treatment for early-stage liver cancer, especially for patients who are ineligible for surgery. Ultrasound (US) is commonly used during procedures as it provides real-time imaging, is widely available, and doesn’t use radiation. Conventionally, doctors must interpret 2D images to locate tumours in a 3D space. This process requires extensive experience and training to perform reliably. Additionally, identifying tumours using US can be challenging, especially when the tumour is confused with non-cancerous nodules or in a hard-to-reach location. These challenges limit the use of ablation procedures in clinical practice. This project aims to investigate how 3D US can improve and facilitate percutaneous thermal liver tumour ablations. It also demonstrated the potential to translate to other clinical oncological applications, such as renal tumour ablation.
</p>

<table align="center" border="0" cellspacing="0" cellpadding="0" style="border:none !important; border-collapse:collapse !important; border-spacing:0 !important; border-top:0 !important; border-bottom:0 !important;">
  <tr>
    <td align="center" width="50%" style="border:none !important; padding:0 !important;">
      <a href="https://www.youtube.com/watch?v=rgaihhQIr80" target="_blank" rel="noopener noreferrer">
        <img src="figs/3DLIVUS_CTV_demonstration_Cool_v.png" 
             alt="CTV News - 3DLIVUS Demonstration" 
             width="90%">
      </a>
      <br>
      <a>🎬 3DLIVUS featured on CTV News (Jan 27, 2023)</a>
    </td>
    <td align="center" width="50%" style="border:none !important; padding:0 !important;">
      <a href="https://youtu.be/hxs5y-deY70" target="_blank" rel="noopener noreferrer">
        <img src="figs/3DLIVUS_demonstration_Cool.png" 
             alt="Schulich School - 3DLIVUS Demonstration" 
             width="90%">
      </a>
      <br>
      <a>🎬 Demonstration by Schulich School of Medicine & Dentistry </a>
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
  <a>Figure 1. (a) Overview of the 3DLIVUS system; (b) 3D US scanning mode.</a>
</div>

<br>
<p align="justify">
For the development of 3DLIVUS system, not only the hardware design and maching, such as the counterbalanced arm and 3D US scanner, we have also developed a robust and efficient arm calibration approach, see the <a href="https://github.com/Xingorno/Robotic-arm-calibration-method-from-scratch" target="_blank" rel="noopener noreferrer">link</a>.  
</p>

<p align="justify">
  Figure 2 shows our proposed framework for integrating 3D US into the standard clinical ablation workflow, which advanced the capabities of 3D US imaging in improving percutaneous tumour ablation, demonstrating the potential to expand the therapeutic role of 3D US in clinical interventions. In detail, the ablation workflow is enhanced with intra-procedural tumour coverage (project 2), tumour identification (project 3), multimodal visualization and instrument tracking (project 4).
</p>
<div align="center">
  <img src="figs/3DLIVUS_integration_framework_black.png" alt="3DLIVUS frame" width="80%">
  <br>
  <a>Figure 2. Framework for 3D US integration into conventional 2D US guidance. (a) 3DLIVUS system; (b) intra-procedural guidance. Note: the role of 3D US is highlighted in a brown block. (Regi: Registration, Recon: 3D US reconstruction)</a>
</div>

## 3D US Acquisition & Clinical Trial
### How does 3DLIVUS acquire images during the procedure?

<p align="justify">
  The 3D US acquisition is fully automatic. During the procedure, the physician/sonographer first needs to place the conventional US probe on the target area of the patient. Then, the probe can be automatically driven by the 3D US scanner to acquire a sequence of 2D US images, which are used for 3D US reconstruction. The whole process (including reconstruction) takes around 7-12 seconds.
</p>

<p align="center">
  <a href="https://youtu.be/NFdtQTTbtVk" target="_blank" rel="noopener noreferrer">
    <img src="figs/3DLIVUS_3DUS scanning_v.png" 
         alt="3DLIVUS image acquisition" 
         width="60%">
  </a>
  <br>
  <a>🎬 Watch the 3DLIVUS system demonstration on image acquisition.</a>
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



<table align="center" border="0" cellspacing="0" cellpadding="0" style="border:none !important; border-collapse:collapse !important; border-spacing:0 !important; border-top:0 !important; border-bottom:0 !important;">
  <tr>
    <td align="center" width="50%" style="border:none !important; padding:0 !important;">
        <img src="figs/Assessment_1.png" 
             alt="Assessment 1" 
             width="90%">
      <!-- <br> -->
      <a>Tumour coverage assessment on 2D US</a>
    </td>
    <td align="center" width="50%" style="border:none !important; padding:0 !important;">
        <img src="figs/Assessment_2.png" 
             alt="Assessment 2" 
             width="90%">
      <!-- <br> -->
      <a>Tumour coverage assessment with surrounding structures </a>
    </td>
  </tr>
</table>

### 3D US-based Tumour Coverage Evaluation
<p align="justify">
To demonstrate that, we conducted a clinical trial from 2021 to 2022. In this trial, we collected data from 12 patients, including 8 cases treated with RFA, 4 cases with MWA. 
As shown in this figure, we firstly manually segmented both the tumour and the needle in 3D US images. The ablation zone was then estimated based on the manufacturer’s guidelines. 
Next, we calculated the surface distances between the tumour and the estimated ablation zone. To validate, we compared the results with clinical outcomes, which were obtained from follow-up CT/MRI images. As a result, in conventional 2D US, 9 out of 12 cases were predicted correctly. However, with our 3D US approach, the accuracy improved to 11 out of 12 cases. For the remaining case, the discrepancy was due to new disease progression, rather than a limitation of the 3D US-based estimation. Overall, these results highlight that our 3D US approach provided valuable and reliable information for all cases, demonstrating its potential to enhance tumour coverage assessment in ablation procedures.
</p>

<br>
<div align="center">
  <img src="figs/Tumour_coverage_compare.png" alt="3DLIVUS assessment" width="80%">
  <br>
  <a>Figure 3. Comparison of tumour coverage evaluation on 2D and 3D US.</a>
</div>


### 3D US-based Needle Adjustment (If required)

<p align="justify">
The next question is: is it possible to optimize those untreated tumours using 3D US during the procedure? To address that, we developed a novel margin uniformity approach to optimize the needle position. The top row shows the different clinical cases, which could happen during the procedure. For each case, our approach generates a 2D plot, as shown in the second row. This plot provides the information on how to adjust the needle.
</p>
<div align="center">
  <img src="figs/Needle adjustment.png" alt="3DLIVUS assessment" width="80%">
  <br>
  <a>Figure. 3D US-based needle adjustment.</a>
</div>
<br>
<p align="justify">
Here is a patient case that requires needle adjustment for complete tumour coverage.
</p>
<div align="center">
  <img src="figs/needle_adjustment_patient.png" alt="3DLIVUS assessment" width="80%">
  <br>
  <a>Figure. 3D US-based needle adjustment case on a patient.</a>
</div>

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

<p align="justify">
  In conventional US guidance, some liver tumours have low conspicuity or are nearly undetectable when imaging small lesions or tumours located in challenging regions, such as the liver dome (see Fig. X left). In addition, tumour mimics, such as regenerative nodules and prior ablation sites, may cause further confusion, making it even more challenging for physicians to accurately identify the tumour, as shown in Fig. right. 

</p>
<br>
<table align="center" border="0" cellspacing="0" cellpadding="0" style="border:none !important; border-collapse:collapse !important; border-spacing:0 !important; border-top:0 !important; border-bottom:0 !important;">
  <tr>
    <td align="center" width="50%" style="border:none !important; padding:0 !important;">
        <img src="figs/Invisible_tumours_1.png" 
             alt="Invisible tumour 1" 
             width="90%">
      <br>
      <a> Left: invisible tumour in US; Right: visible tumour in MRI</a>
    </td>
    <td align="center" width="50%" style="border:none !important; padding:0 !important;">
        <img src="figs/Invisible_tumours_2.png" 
             alt="Invisible tumour 2" 
             width="80%">
      <br>
      <a> Left: benign regenerative nodule; Right: malignant HCC</a>
    </td>
  </tr>
</table>

### Our proposed 2D US-to-CT/MRI registration solution
<p align="justify">
The idea of our proposed method is to divide the direct 2D US-to-CT or MRI registration into two components, which are 3D US-to-CT or MRI registration and 2D US-to-3D US registration. This decomposition strategy could significantly reduce the computational burden for registration algorithms. In addition, the introduction of 3D US images does not increase the clinical workload complexity. The 3D US image acquisition only requires 7s-12s for a single image, and this image can also improve intra-procedure tumour coverage, as demonstrated previously. For this project, we developed a series of registration methods, including <a href="https://github.com/Xingorno/3DUS-CT-or-MRI-Rigid-Registration" target="_blank" rel= "noopener noreferrer">rigid 3D US-to-CT/MRI registration</a>, <a href="https://github.com/Xingorno/TPS-based-Interactive-Deformable-Registration" target="_blank" rel= "noopener noreferrer">deformable 3D US-to-CT/MRI registration</a> and <a href="https://github.com/Xingorno/DeepRegS2V" target="_blank" rel= "noopener noreferrer">rigid 2D-to-3D US registration</a>.
</p>
<br>
<div align="center">
  <img src="figs/registration_workflow.png" alt="registration" width="80%">
  <br>
  <a>Figure. Registration overview of 2D US-to-CT/MRI images</a>
</div>

### Clinical results
Here are some results on humans.
<p align="center">
  <a href="https://www.youtube.com/watch?v=88EfB2hzf-8" target="_blank" rel="noopener noreferrer">
    <img src="figs/3DUS-to-CTorMRI_registration_result_v.png" 
         alt="3DLIVUS registration: 3D US-to-CT/MRI" 
         width="70%">
  </a>
  <br>
  <a>🎬 3DLIVUS registration: 3D US-to-CT/MRI.</a>
</p>
<br>
<p align="center">
  <a href="https://www.youtube.com/watch?v=BHfTiwmbq2c" target="_blank" rel="noopener noreferrer">
    <img src="figs/2DUS-to-CTorMRI_registration_result_v.png" 
         alt="3DLIVUS registration: 2D US-to-CT/MRI" 
         width="80%">
  </a>
  <br>
  <a>🎬 3DLIVUS registration: 2D US-to-CT/MRI.</a>
</p>

## Project 4: Needle Identification (Ongoing...)

### Why improve needle tracking?

<a align="justify">
  Needle’s active tip determines the location of the generated ablation zone, directly impacting the tumour coverage and treatment effectiveness. However, accurate needle identification remains a challenge due to several factors: (1) Due to the in-plane insertion requirement, the needle often veers away from the imaging plane. (2) And the needle often shows poor image quality, especially when inserted at a steep angle or at greater depths. (3) In addition, needle mimics such as the boundary of the gallbladder can resemble the needle, further complicating identification and increasing the risk of misinterpretation. These challenges highlight the need for improved needle tracking methods to enhance accuracy, confidence, and treatment success in ultrasound-guided ablation, as shown in the video below.
</a>
<br>
<p align="center">
  <a href="https://youtu.be/N8PFr8XevkU" target="_blank" rel="noopener noreferrer">
    <img src="figs/needle tracking_v.png" 
         alt="3DLIVUS tracking: Needle tracking" 
         width="60%">
  </a>
  <br>
  <a>🎬 3DLIVUS tracking: Needle tracking.</a>
</p>
<br>

### What are we doing?

<p align="justify">This project is still ongoing. The patient dataset has already been collected and annotated. 
<strong>The update is coming soon!</strong>
</p>
