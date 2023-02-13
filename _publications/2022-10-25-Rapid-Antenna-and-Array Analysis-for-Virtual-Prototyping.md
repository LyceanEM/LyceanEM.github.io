---
title: "Rapid Antenna and Array Analysis for Virtual Prototyping"
collection: publications
permalink: /publication/2021-04-21-Conformal-Antenna-Array-Design-using-Aperture-Synthesis-and-On-platform-modelling
excerpt: 'Demonstration of the workflow for rapid antenna array design and analysis using LyceanEM'
date: 2022-10-25
venue: 'Radar 2022'
paperurl: 'https://ieeexplore.ieee.org/document/10038925'
citation: 'T. G. Pelham, "Rapid antenna and array analysis for virtual prototyping" International Conference on Radar Systems (RADAR 2022), Hybrid Conference, Edinburgh, UK, 2022, pp. 278-282, doi: 10.1049/icp.2022.2330'
---
The increased use of radar systems in new form factors from automotive to small unmanned aerial vehicles requires the development of robust and accessible methods for virtual prototyping. Allowing a project team to evaluate the influence of platform structure, antenna or array geometry and beamforming architecture on overall system performance. Using spatial measurements of a Sea Searcher X band radar as an example, LyceanEM is used to predict the influence of reflector shape on maximum achievable directivity, and predicted antenna pattern, compared with full electromagnetic solver (CST) at 9.3GHz. LyceanEM showed a correlation of 0.8 between the predicted and full solver antenna pattern, predicting a maximum directivity of 19.36dBi, compared to 21.97dBi for CST, using 109 seconds of runtime, versus 37 hours for the time domain solver.

![Sea Searcher Radar](/images/seasearcher.png "Sea Searcher Radar with Rotator and RF Electronics")
*Figure 1 Sea Searcher Radar*

The measured antenna aperture has a maximum directivity enevelope which can be predicted very rapidly using LyceanEM, and this can then be used to move forward on designs. In this case, the workflow is demostrating the analysis of an exsisting antenna, so the prediction is based upon a fixed horn illuminator and no beamforming. The maximum directivity envelope is shown in Figure 2, while the predicted antenna patterns are shown in Figures 3 and 4.

![Maximum Directivity Envelope](/images/directivitymap.png "Maximum directivity envelope for reflector")

*Figure 2 Sea Searcher Reflector Maximum Directivity Envelope*

![Dtheta](/images/predictedDtheta.png "Predicted Etheta antenna directivity")

*Figure 3 Etheta polarisation directivity pattern*

![Dtheta](/images/predictedDphi.png "Predicted Ephi antenna directivity")

*Figure 4 Ephi polarisation directivity pattern*

