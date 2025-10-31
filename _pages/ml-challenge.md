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

## Challenge Details

- **Objective**: Develop Theoretical, analytical or ML models that can accurately predict the gain profile of commercial EDFAs under various operating conditions
- **Dataset**: We will provide a large EDFA gain profile dataset which is collected three years ago, and a small amount of the EDFA measurements we collect recently aiming the three technique issue we mentioned above.
- **Evaluation**: Models will be scored based on prediction accuracy under an hidden testset with three aspects mentioned above.

## Dataset repo

- We will provide all the codes for pre-processing the measurements data and a simple ML-based model just for reference
- Please refer to the [dataset website](https://github.com/ofc-ml-challenge/ofc-ml-challenge-test) for more details

## Results submission 

- Please submit your predicted `csv` file to this year [Kaggle submission platform](https://www.kaggle.com/t/6b41bccbf1a04782b7b3f4bc3f21041b)
- We will also evaluate your model based on factors such as model size, inference time, and the novelty of the model architecture. Please create a GitHub repository ([example](https://github.com/ofc-ml-challenge/ofc-ml-challenge-test)) and provide clear step-by-step instructions on how to run your model.

## Acknowledgement
- Event organizer: [OFC](https://www.ofcconference.org/) 
- PI: Tingjun Chen, Danniel Kilper
- Student host: Zehao Wang, Mingzhe Han

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/ZehaoWang.jpg" class="img-fluid rounded z-depth-1" caption="Zehao Wang" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/MingzheHan.jpg" class="img-fluid rounded z-depth-1" caption="Mingzhe Han" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/tingjunchen.jpg" class="img-fluid rounded z-depth-1" caption="Tingjun Chen" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/dankilper.jfif" class="img-fluid rounded z-depth-1" caption="Danniel Kilper" %}
    </div>
</div>
