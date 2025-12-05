---
layout: page
title: ML Challenge
permalink: /ml-challenge/
# description: Details and submission information for the 1st OFC 2026 ML Challenge.
nav: true
nav_order: 2
---

This year's challenge focuses on training models to predict gain profiles for **Commercial Erbium-Doped Fiber Amplifiers (EDFAs)**. EDFAs are critical components in optical communication systems, and accurate gain profile prediction is essential for optimizing network performance and reliability, especially under dynamic channel loading conditions.

## Motivation

EDFA gain profile prediction is crucial for:

- Network planning and optimization
- Dynamic power management
- System reliability and performance monitoring
- Cost-effective network operations

Especially under dynamic channel loading conditions. Recently, researchers acheives high accuracy over gain profile predictions, but there are still some challenge unsolved. In our testing, we will evaluate the following three aspects of your EDFA DWDM channel gain model:

- EDFA channel gain aging effect
- Spectrum hole burning effect
- Unmeasured gain and tilt settings of EDFA

Here are the examples for typical gain spectrum under these three test goals, detailed description can be found in the [kaggle competition description](https://www.kaggle.com/competitions/ofc-2026-ml-challenge/overview)

- EDFA channel gain aging effect
    - EDFA gain profile changes over 3 years on the same device 
    - We will only provide a small amount of the EDFA gain profile with aging effect for the training set

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/edfa_aging.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

- Spectrum hole burning effect
    - Gain profile especially under goalpost channel loading
    - We will not provide any goalpost channel loading data for the training set

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/edfa_shb.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

- Unmeasured gain and tilt settings of EDFA
    - We will NOT provide the gain profile data for 20 dB and test your model generizability for unseen gain
    - We will provide small amount of the EDFA gain profile with tilt and a larger dataset with all tilt equaling to 0 dB, and test your model performance on the tilted gain 

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/edfa_unseen.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>


## Challenge Details

- **Objective**: Develop Theoretical, analytical or ML models that can accurately predict the gain profile of commercial EDFAs under various operating conditions
- **Dataset**: We will provide a large COSMOS EDFA gain profile dataset which is collected three years ago, and a small amount of the EDFA measurements we collect recently aiming the three technique issue we mentioned above.
- **Evaluation**: Models will be scored based on prediction accuracy under an hidden testset with three aspects mentioned above.

## Dataset repo and submission platform

### Dataset and example code 
- We will provide all the codes for pre-processing the measurements data and a simple ML-based model just for reference
- Please refer to the [dataset website](https://github.com/ofc-ml-challenge/ofc-ml-challenge-data-code) for more details
- Dataset repo including:
<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/Github_diagram.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

### Submission platform 
- We provide detailed tutorial for the dataset explaination
- This is the official submission platform where you can see your score on the test set for real time
- There is a discussion panel on the competition page where you can post your questions 
- Submission platform including:
<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/Kaggle_diagram.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

## Results submission 

- Please submit your predicted `csv` file to this year [Kaggle submission platform](https://www.kaggle.com/competitions/ofc-2026-ml-challenge/overview)
- We will also evaluate your model based on factors such as model size, inference time, and the novelty of the model architecture. Please create a GitHub repository ([example](https://github.com/ofc-ml-challenge/ofc-ml-challenge-data-code)) and provide clear step-by-step instructions on how to run your model.

## Organizer
<!-- - Event organizer: [OFC](https://www.ofcconference.org/) 
- PI: Tingjun Chen, Danniel Kilper
- Student host: Zehao Wang, Mingzhe Han -->

<style>
  .caption {
    font-size: 1.2em;
    font-weight: 500;
    margin-top: 0.5em;
  }
  .row.mt-3:first-of-type figure img {
    height: auto;
    width: 100%;
    object-fit: contain;
    object-position: center;
  }
  .row.mt-3 figure img[src*="Github_diagram"],
  .row.mt-3 figure img[src*="Kaggle_diagram"] {
    height: auto !important;
    width: 75% !important;
    object-fit: contain !important;
    object-position: center;
    display: block;
    margin: 0 auto;
  }
  .row.mt-3 figure img[src*="logo_ofc"] {
    height: auto !important;
    width: 50%;
    object-fit: contain;
    object-position: center;
  }
  .row.mt-3 figure img[src*="edfa_aging"],
  .row.mt-3 figure img[src*="edfa_shb"],
  .row.mt-3 figure img[src*="edfa_unseen"] {
    height: auto !important;
    width: 50% !important;
    object-fit: contain;
    object-position: center;
    display: block;
    margin: 0 auto;
  }
  .row.mt-3 figure img[src*="ZehaoWang"],
  .row.mt-3 figure img[src*="MingzheHan"] {
    height: auto !important;
    width: 50% !important;
    object-fit: contain;
    object-position: center;
    display: block;
    margin: 0 auto;
  }
  .row.mt-3 figure[class*="img-fluid"] {
    text-align: center;
  }
</style>

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/tingjunchen.jpg" class="img-fluid rounded z-depth-1" caption="Tingjun Chen" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/dankilper.jfif" class="img-fluid rounded z-depth-1" caption="Danniel Kilper" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/Camille.png" class="img-fluid rounded z-depth-1" caption="Camille Delezoide" %}
    </div>
</div>

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/logo_ofc_with_tag_blue.png" class="img-fluid rounded z-depth-1" caption="Event Organizer" %}
    </div>
</div>

## Acknowledgement

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/ZehaoWang.jpg" class="img-fluid rounded z-depth-1" caption="Zehao Wang" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/MingzheHan.jpg" class="img-fluid rounded z-depth-1" caption="Mingzhe Han" %}
    </div>
</div>
