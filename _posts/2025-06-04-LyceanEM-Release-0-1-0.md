---
title: 'LyceanEM Release 0.1.0'
date: 2025-6-04
permalink: /posts/2025/6/LyceanEM-Release-0-1-0/
tags:
  - SCOPES
  - Space Based Solar Power
  - LyceanEM
  - Department for Energy Security and Net Zero
---


I'm delighted to announce the version 0.1.0 release of hashtag#LyceanEM. The support of the Net Zero Innovation Portfolio has allowed us to complete the first major release of our development roadmap. This includes :

Computational efficiency and scalability: The computational efficiency of LyceanEM has been improved, and it can now be used on a wider range of hardware platforms, including desktop computers and high-performance computing (HPC) clusters with a single conda command and simplified dependencies. This will make LyceanEM more accessible to a wider range of users. This has been demonstrated for antenna arrays with up to a million antennas so far. Appropriate HPC compute should enable the modelling of antenna arrays suitable for space-based solar power and other applications with over a billion antenna elements.

Core propagation engine: The core propagation engine of LyceanEM has been upgraded to include more realistic models of lossy propagation and atmospheric effects for each layer of the atmosphere. This will make LyceanEM more accurate and versatile for a wider range of applications. Atmospheric propagation models have been added to LyceanEM, including the ITU-R P.676-11 model for atmospheric absorption and rain attenuation. 

Modelling fidelity: New features and functions have been added to LyceanEM that will allow users to model electromagnetic systems with greater fidelity. This includes support for importing antenna patterns and time domain sources, as well as the development of open source standards for antenna array designs, antenna patterns and field sources, and wireless power transfer.



----------------------

LyceanEM Release 0.1.0
------------------------------------------------------------

There is one slight fly in the ointment which is that due to the need to build the examples on a computer with a GPU I have not yet been able to deploy interactive plots to make the best use of pyvista's capabilities. However, any interested developer or engineer with an Nvidia GPU can download the examples and run them within about 10 minutes for all of them.
In addition, the benefit of a website like this is that I can embed the resulting plots as exported html pages, allowing the interested to interact with them without the need for any simulations or installation.

<iframe src="/files/example02results.html" height="800" width="1000"></iframe>

The first example is the antenna array pattern for the 10GHz conformal antenna array mounted on the demo UAV and drawn from example 02. This shows the resultant antenna array pattern without any beamforming in particular. 

<iframe src="/files/example05results.html" height="800" width="1000"></iframe>

The second example is the achived maximum beamformed directivity pattern for the same antenna array. This can be achieved with the use of a function call to predict the antenna element patterns for the demo conformal array, then a second function call to beamform the resultant patterns with a number of different algorithms. The resultant pattern of achiveved directivity at each command angle can then be plotted. This gives an excellent overview of the capability of LyceanEM for assessing the overall antenna array performance in terms of controllable directive gain.

Space-based Solar Power
-------------------------

`LyceanEM` has been developed by the SCOPES project, funded by the Net Zero Innovation Portfolio, to support the development of Space-based Solar Power (SBSP) systems. The project is a collaboration between the University of Bristol and Virtus Solis, and aims to develop the computational tools required to design and operate the gigascale antenna arrays required for SBSP. To this end the release of version 0.1.0 marks the first open release of `LyceanEM` with a CUDA engine which is capable of splitting a model across multiple GPUs with the right scripting, and simulating truly enormous models in a short space of time.

**Wavefront Beamforming for Receiver**
<iframe src="/files/SBSP_Aperturev1.html" height="800" width="1000"></iframe>

**Wavefront Beamforming for Terrain**
<iframe src="/files/SBSP_Terrainv1.html" height="800" width="1000"></iframe>

**Retrodirective Beamforming for Receiver**
<iframe src="/files/SBSP_Aperturev2.html" height="800" width="1000"></iframe>

**Retrodirective Beamforming for Terrain**
<iframe src="/files/SBSP_Terrainv2.html" height="800" width="1000"></iframe>

The third dynamic example is one which is particularly interesting, and is so large it really has to be shown in four parts. This is because it shows the resultant power density for a scale model of a Space-based Solar Power system, with the receiver located just outside Walton-in-Gordano. The map tile use is drawn from the National Lidar Programme, and includes the receiving antenna array with 1 million antenna elements. This array is illuminated from a transmitting antenna array located over 5.9km away on the elevation and azimuth bearing which a notional geostationary Space-based solar power plant might be located. This example demonstrates a power transfer efficiency of 85% using Retrodirective Beamforming, compared to only 82% using Wavefront Beamforming. This equates to a total received power from the station of 191.7kW.

The transmitter was specified as a circular antenna array with a diameter of 34.4m with 250,000 elements. The received power at the receiver based upon propagation from the transmitter through the lower atmosphere, with comparison of three different beamforming schemes was simulated in under six hours, an impressive feat for a general model coping with $` 2.5\times10^{11}`$ independant paths in a complex environment.

This is a significant step forward in the development of LyceanEM, and demonstrates the potential of the software to support the development of Space-based Solar Power systems. The next steps will be to continue to improve the computational efficiency and scalability of LyceanEM, and to add more features and functions to support a wider range of applications.


<script src="https://utteranc.es/client.js"
        repo="LyceanEM/LyceanEM.github.io"
        issue-term="LyceanEM-Release-0-1-0"
        theme="github-light"
        crossorigin="anonymous"
        async>
</script>