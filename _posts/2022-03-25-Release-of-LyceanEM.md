---
title: 'Release of LyceanEM'
date: 2022-3-25
permalink: /posts/2022/3/Release-of-LyceanEM/
tags:
  - LyceanEM
---

LyceanEM, the electromagnetics software I have been developing to support my research is now open for anybody to use. If you have an interest in communications, antennas, or radar then LyceanEM can help.

---

I am delighted to announce the publication of LyceanEM under the GPL-3.0 License. This model is written in Python, but uses the excellent [Numba](https://numba.readthedocs.io/en/stable/) package to accelerate the calculations using [CUDA](https://www.nvidia.com/en-gb/geforce/technologies/cuda/). Therefore, currently an Nvidia GPU capable of using CUDA is required for installation.

That said, LyceanEM allows the user to carry out a wide range of tasks relating to antenna arrays and antennas within a complex system. For those interested in systems design, LyceanEM can predict the maximum directivity envelope for any aperture on a platform rapidly, reducing the technical and project risk of antenna array design. This can then be improved by moving from the maixmum directivity envelope to the effects of array polarisation, beamforming architecture, and beamforming algorithms on the array performance.

This is part of the workflow made possible within LyceanEM, and demonstrated in my paper [Conformal Antenna Array Design Using Aperture Synthesis and On-Platform Modelling](https://ieeexplore.ieee.org/document/9408625).

The documentation can be found [here](https://lyceanem-python.readthedocs.io/en/latest/), and the code [here](https://github.com/LyceanEM/LyceanEM-Python). I will be continuing to develop the codebase, extending the models and providing examples for each major function.

If you have any questions about LyceanEM, how to use it, or help implementing it for your desired end use please get in contact.

<script src="https://utteranc.es/client.js"
        repo="LyceanEM/LyceanEM.github.io"
        issue-term="Release-of-LyceanEM"
        theme="github-light"
        crossorigin="anonymous"
        async>
</script>
