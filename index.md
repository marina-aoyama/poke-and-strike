---
layout: default
title: "Poke and Strike: Learning Task-Informed Exploration Policies"
---

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

# Poke and Strike:<br>Learning Task-Informed Exploration Policies

<a href="https://scholar.google.com/citations?user=OJmSDo8AAAAJ&hl=ja&oi=ao" target="_blank" style="color: #5faee3; text-decoration: none;">Marina Y. Aoyama</a><sup>1</sup>, 
<a href="https://scholar.google.co.jp/citations?user=1L5kTRcAAAAJ&hl=en&oi=sra" target="_blank" style="color: #5faee3; text-decoration: none;">Joao Moura</a><sup>1</sup>, 
<span style="color: #5faee3; text-decoration: none;">Juan Del Aguila Ferrandis</span><sup>1</sup>
<a href="https://scholar.google.com/citations?user=JdRs1sQAAAAJ&hl=ja&oi=ao" target="_blank" style="color: #5faee3; text-decoration: none;">Sethu Vijayakumar</a><sup>1</sup>

<sup>1</sup>School of Informatics, The University of Edinburgh, UK

Conference on Robot Learning (CoRL) 2025 

<!-- <div class="button-container">
  <a href="#" class="my-button disabled">
    <span class="icon"><i class="fas fa-file-alt"></i></span>
    <span>Paper</span>
  </a>
  
  <a href="#" class="my-button disabled">
    <span class="icon"><i class="fas fa-video"></i></span>
    <span>Video</span>
  </a>
  
  <a href="#" class="my-button disabled">
    <span class="icon"><i class="fab fa-github"></i></span>
    <span>Code</span>
  </a>
</div> -->

<div class="button-container">
  <a href="https://openreview.net/forum?id=SUqMCzslNH#discussion" class="my-button">
    <span class="icon"><i class="fas fa-file-alt"></i></span>
    <span>Paper</span>
  </a>

  <a href="https://arxiv.org/pdf/2509.00178" class="my-button">
    <span class="icon"><i class="fas fa-file-alt"></i></span>
    <span>ArXiv</span>
  </a>
  
  <a href="https://www.youtube.com/watch?v=tvM0A5WxVfM&t=1s" class="my-button">
    <span class="icon"><i class="fas fa-video"></i></span>
    <span>Video</span>
  </a>
  
  <a href="#" class="my-button disabled">
    <span class="icon"><i class="fab fa-github"></i></span>
    <span>Code</span>
  </a>
</div>

<video width="800" height="450" controls loop autoplay playsinline webkit-playsinline style="margin-top: 2rem;">
  <source src="videos/sliding_corl_myvoice_3min_staticqr.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

<h2>Abstract</h2>
<div style="text-align: justify;">
  <p>
    In many dynamic robotic tasks, such as striking pucks into a goal outside the reachable workspace, the robot must first identify the relevant physical properties of the object for successful task execution, as it is unable to recover from failure or retry without human intervention. To address this challenge, we propose a <b>task-informed exploration approach, based on reinforcement learning</b>, that trains an exploration policy using rewards automatically generated from the sensitivity of a privileged task policy to errors in estimated properties. We also introduce an uncertainty-based mechanism to determine when to transition from exploration to task execution, ensuring sufficient property estimation accuracy with minimal exploration time. Our method achieves a <b>90% success rate</b> on the striking task with an average <b>exploration time under 1.2 seconds</b>—significantly outperforming baselines that achieve at most 40% success or require inefficient querying and retraining in a simulator at test time. Additionally, we demonstrate that our task-informed rewards capture the relative importance of physical properties in both the striking task and the classical CartPole example. Finally, we validate our approach by demonstrating its ability to identify object properties and adjust task execution in a physical setup using the KUKA iiwa robot arm. 
    </p>
</div>

<h2>Method</h2>
<div style="text-align: justify;">
  <p>
We propose a task-informed exploration approach, based on reinforcement learning, that trains an <b>exploration policy using rewards automatically generated from the sensitivity of a privileged task policy to errors in estimated properties</b>. We also introduce an <b>uncertainty-based mechanism to determine when to transition from exploration to task execution</b>, ensuring sufficient property estimation accuracy with minimal exploration time. 
approach by demonstrating its ability to identify object properties and adjust task execution in a physical setup using the KUKA iiwa robot arm. 
    </p>
</div>

<img src="videos/method_image.png" 
     width="800" 
     height="450" 
     alt="Method illustration" 
     style="display: block; margin: 0 auto;">

## Results 

<div style="display: grid; grid-template-columns: repeat(2, 1fr); gap: 3rem 5rem; max-width: 900px; margin: auto;">

  <!-- Column Headers -->
  <div style="text-align: center; font-weight: bold; font-size: 1rem; font-family: monospace;margin-bottom: 0.1rem;">Striking</div>
  <div style="text-align: center; font-weight: bold; font-size: 1rem; font-family: monospace;margin-bottom: 0.1rem;">Edge Pushing</div>

  <div style="text-align: center;">
    <div style="font-size: 0.85rem; color: #555; margin-bottom: 1rem;"> Learned to poke and strike </div>
    <video width="400" controls muted loop autoplay playsinline webkit-playsinline>
      <source src="videos/striking_main_nosound.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
  </div>

  <div style="text-align: center;">
    <div style="font-size: 0.85rem; color: #555; margin-bottom: 1rem;"> Learned to rotate and push to the edge </div>
    <video width="400" controls muted loop autoplay playsinline webkit-playsinline>
      <source src="videos/egg_main_nosound.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
  </div>

  <div style="text-align: center;">
    <div style="font-size: 0.85rem; color: #555; margin-bottom: 1rem;"> Pucks with 3 different friction levels: 8/9 </div>
    <video width="400" controls muted loop autoplay playsinline webkit-playsinline>
      <source src="videos/striking_trials_nosound.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
  </div>

  <div style="text-align: center;">
    <div style="font-size: 0.85rem; color: #555; margin-bottom: 1rem;"> Box with eggs on 2 different sides: 8/10 </div>
    <video width="400" controls muted loop autoplay playsinline webkit-playsinline>
      <source src="videos/egg_trials_nosound.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
  </div>

  <div style="text-align: center;">
    <div style="font-size: 0.85rem; color: #555; margin-bottom: 1rem;"> Friction </div>
    <video width="400" controls muted loop autoplay playsinline webkit-playsinline>
      <source src="videos/striking_estimates_nosound.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
  </div>

  <div style="text-align: center;">
    <div style="font-size: 0.85rem; color: #555; margin-bottom: 1rem;"> CoM x </div>
    <video width="400" controls muted loop autoplay playsinline webkit-playsinline>
      <source src="videos/egg_estimates_nosound.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
  </div>
</div>

### Tricking the robot

<video width="600" height="450" controls muted loop autoplay playsinline webkit-playsinline>
  <source src="videos/striking_trick_the_robot.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

### Can the robot identify the shifted weight? 

<video width="600" height="450" controls muted loop autoplay playsinline webkit-playsinline>
  <source src="videos/edge_pushing_egg.m4v" type="video/mp4">
  Your browser does not support the video tag.
</video>

### Sensitivity modeling and exploration rewards generation

<video width="600" height="450" controls muted loop autoplay playsinline webkit-playsinline>
  <source src="videos/sensitivity_cropped.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

## BibTex 
<div class="citation-wide">
  <div style="position: relative; max-width: 950px; margin: 0 auto;">
    <button onclick="copyBibtex(this)" style="
      position: absolute;
      top: 0.5rem;
      right: 0.5rem;
      font-size: 0.75rem;
      padding: 0.3rem 0.6rem;
      border: none;
      background: #ddd;
      border-radius: 4px;
      cursor: pointer;
      z-index: 1;
    ">Copy</button>
    <pre style="
      font-family: monospace;
      font-size: 0.85rem;
      background: #f5f5f5;
      border: 1px solid #ccc;
      border-radius: 6px;
      padding: 2rem 0.75rem 0.75rem 0.75rem;  /* extra top padding for the button */
      overflow-x: auto;
      white-space: pre-wrap;
      word-break: break-word;
    "><code id="bibtex-block">@inproceedings{
      aoyama2025poke,
      title={Poke and Strike: Learning Task-Informed Exploration Policies},
      author={Marina Y. Aoyama and Joao Moura and Juan Del Aguila Ferrandis and Sethu Vijayakumar},
      booktitle={9th Annual Conference on Robot Learning},
      year={2025},
      }
    </code></pre>
  </div>
</div>

<script>
  function copyBibtex(button) {
    const code = button.nextElementSibling.querySelector('code');
    navigator.clipboard.writeText(code.textContent).then(() => {
      button.textContent = 'Copied!';
      setTimeout(() => { button.textContent = 'Copy'; }, 2000);
    });
  }
</script>



