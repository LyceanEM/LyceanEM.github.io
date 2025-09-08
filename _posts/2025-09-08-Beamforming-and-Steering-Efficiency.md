---
title: 'Beamforming and Steering Efficiency in Phased Array Antennas'
date: 2025-9-08
permalink: /posts/2025/9/Beamforming-and-Steering-Efficiency/
tags:
  - Antennas
  - Phased Arrays
  - Beamforming
  - LyceanEM
---

Comparing the performance of different antenna array designs and beamforming methods can be challenging, especially when conformal antenna arrays are also considered in the design arena. The boresight gain and half power beamwidth are often used to compare antenna arrays and antenna designs, and the ideal figures are easy to calculate for a planar aperture at a given frequency. However, this tells us little about the performance of the antenna array away from boresight, and is of limited use for conformal antenna arrays. Quite a number of years ago I came across a very useful concept called steering efficiency, and the steering efficiency product, which can be used to compare different antenna array architectures and beamforming methods, accounting for different frequencies and array sizes.


----------------------


Beamforming and Steering Efficiency in Phased Array Antennas
------------------------------------------------------------

The maximum potential gain of an antenna array is given by the effective area of the array aperture and the wavelength of interest, as discussed by
Hannan in the `Element-Gain Paradox for a Phased-Array Antenna` [1]. This can be combined with the ideal element pattern for an antenna array element  and the direction of interest in order to calculate the maximum achievable gain for an antenna array at any angle $g_{max}(\theta,\phi)$, as shown in **Figure 1**.

![Ideal Array Element Pattern](/images/cos_pattern.png)
**Figure 1: Ideal Array Element Pattern for an array element.**

What this means for beamforming, is that for a planar antenna array there is a fundamental limit on how much gain can be achieved at any angle. This can be addressed with different approaches in antenna design, but fundamentally these are based upon extending the array from a planar surface to a more 3D structure. 

$g_{max}(\theta,\phi)=\dfrac{4\pi A}{\lambda^{2}}\cos(\theta)$

While this is a useful result for predicting the performance in isolation of a planar antenna array, it does not function as a useful figure of merit for comparing different antenna array designs, or different beamforming methods. This is where the concept of steering efficiency and steering efficiency product come into play.


Steering Efficiency and Steering Efficiency Product
---------------------------------------------------------
In order to provide a useful assesment of the performance of an antenna array and allow comparison with other antenna array designs, the figure must include the relationship between the achieved gain and the maximum achievable gain, and the effects of scan loss on the antenna array performance. 

The concept of steering efficiency $\eta_{s}$ was proposed by Marin and Hesselbarth in `Figure of Merit for Beam-Steering Antennas` [2]. 


This can be demonstrated using the LyceanEM [Array Beamforming](https://documentation.lyceanem.com/en/latest/auto_examples/05_array_beamforming.html#sphx-glr-auto-examples-05-array-beamforming-py) example for a 10GHz conformal antenna array mounted on a UAV, as shown in **Figure 2**. The achieved gain at each command angle can be calculated using LyceanEM and Wavefront Beamforming, and the steering efficiency calculated.

<iframe src="/files/example05results.html" height="800" width="1000"></iframe>
**Figure 3: Achieved Gain for a 10GHz Conformal Antenna Array mounted on a UAV.**

<video width="800" height="1000" controls loop="" muted = "" autoplay="">
    <source src="https://github.com/LyceanEM/LyceanEM.github.io/raw/refs/heads/master/files/Beamforming_Animation.mp4" type="video/mp4">
</video>

**Figure 4: Animated Achieved Gain for a 10GHz Conformal Antenna Array mounted on a UAV, scanning from -90 to 90 in Azimuth**





[1]  P. Hannan, "The element-gain paradox for a phased-array antenna," in IEEE Transactions on Antennas and Propagation, vol. 12, no. 4, pp. 423-433, July 1964, doi: [10.1109/TAP.1964.1138237](https://ieeexplore-ieee-org.bris.idm.oclc.org/document/1138237)

[2]: J. G. Marin and J. Hesselbarth, "Figure of Merit for Beam-Steering Antennas," 2019 12th German Microwave Conference (GeMiC), Stuttgart, Germany, 2019, pp. 44-47, doi: [10.23919/GEMIC.2019.8698122](https://ieeexplore-ieee-org.bris.idm.oclc.org/document/8698122) 


<script src="https://utteranc.es/client.js"
        repo="LyceanEM/LyceanEM.github.io"
        issue-term="Beamforming-and-Steering-Efficiency"
        theme="github-light"
        crossorigin="anonymous"
        async>
</script>