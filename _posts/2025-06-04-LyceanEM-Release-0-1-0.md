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

<iframe src="/files/example02results.html" height="800" width="1000"></iframe>

The third example is one which is particularly interesting, because it shows the resultant power density for a scale model of a Space-based Solar Power system, with the receiver located just outside Walton-in-Gordano. The map tile use is drawn from the National Lidar Progamme, and includes the receiving antenna array with 1 million antenna elements. This array is illuminated from a transmitting antenna array located over 5km away on the elevation and azimuth bearing which a notional geostationary Space-based solar power plant might be located. This example demonsrates a power transfer efficiency of 85% using Retrodirective Beamforming, compared to only 82% using Wavefront Beamforming. This equates to a total received power from the station of 191.7kW.

<script src="https://utteranc.es/client.js"
        repo="LyceanEM/LyceanEM.github.io"
        issue-term="LyceanEM-Release-0-1-0"
        theme="github-light"
        crossorigin="anonymous"
        async>
</script>