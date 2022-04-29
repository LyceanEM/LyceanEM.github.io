---
title: 'LyceanEM Examples'
date: 2022-4-29
permalink: /posts/2022/4/LyceanEM-Examples/
tags:
  - LyceanEM
---

Addition of examples to the documentation for LyceanEM, found at [examples](https://lyceanem-python.readthedocs.io/en/latest/auto_examples/index.html). The examples cover Aperture Projection, Aperture Modelling, Array Modelling and Beamforming, and modelling physical channels in the Frequency or Time Domain.

---

[Aperture Projection](https://lyceanem-python.readthedocs.io/en/latest/auto_examples/01_aperture_projection.html) 
--------------------
Aperture Projection introduces the most basic level model included in LyceanEM. A frequency domain approach to predicting the maximum directivity envelope for an aperture at a given frequency. The example is based upon an arbitary small UAV with a doubly curved conformal antenna array at 10GHz, but the function itself can be used for a wide range of antenna arrays and platforms, from buildings and integrated mobile communications antenna arrays, to ships or satellites with electrically large antenna arrays. 

[Modelling a Coherently Polarised Aperture](https://lyceanem-python.readthedocs.io/en/latest/auto_examples/02_coherently_polarised_array.html)
--------------------------------------------
The second example is an extension of the Aperture Projection example, introducing an automatic mesh function to populate the aperture with antenna array source points and predicting the overall antenna pattern for the aperture. This also introduces specifying the antenna array polarisation vector which can then be projected onto the conformal surface which is being modelled. This allows simple specification of farfield polarisatoin (Vertical/Horizontal), and automatic generation of suitable array element polarisation vectors.

[Array Beamforming](https://lyceanem-python.readthedocs.io/en/latest/auto_examples/05_array_beamforming.html)
-------------------
Array Beamforming as an example extends the coherently polarised aperture by modelling the array as an antenna array, predicting the element pattern of all specified elements, and then introducing helper functions which allow the user to automatically map the beamformed directivity envelope of the antenna array. This example also introduces the concept of steering efficiency, allowing the array to be evaluated in terms of the coverage which is 'reachable' within 3dB of the maximum directivity of the array.

[Modelling a Physical Channel in the Frequency Domain](https://lyceanem-python.readthedocs.io/en/latest/auto_examples/03_frequency_domain_channel_modelling.html)
-----------------------------------------------------
This example is based upon the paper [Polarimetric Scattering with Discrete Raytracing for OTA Analysis](https://ieeexplore.ieee.org/document/9410981). This example introduces the model functions within LyceanEM for modelling physical channels in the frequency domain, and producing the scattering parameters of the channel.

[Modelling a Physical Channel in the Time Domain](https://lyceanem-python.readthedocs.io/en/latest/auto_examples/04_time_domain_channel_modelling.html)
-----------------------------------------------------
This example is a time domain extension of the frequency domain one. Using the Time domain model included in LyceanEM in order to model the same scenario, but producing a time of flight model of the propagation with a specific illuminating waveform. The resultant received signal at the receiving antenna is then subjected to a fourier transform to produce an equivalent scattering parameter to that produced by the frequency domain example. 


Full Documentation
------------------
The documentation can be found [here](https://lyceanem-python.readthedocs.io/en/latest/), and the code [here](https://github.com/LyceanEM/LyceanEM-Python). I will be continuing to develop the codebase, extending the models and providing examples for each major function.

If you have any questions about LyceanEM, how to use it, or help implementing it for your desired end use please get in contact.

<script src="https://utteranc.es/client.js"
        repo="LyceanEM/LyceanEM.github.io"
        issue-term="LyceanEM-Examples"
        theme="github-light"
        crossorigin="anonymous"
        async>
</script>
