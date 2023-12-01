---
title: 'Vehicular Dataset with Spirent and Cardiff University'
date: 2023-11-24
permalink: /posts/2023/11/Vehicular-Dataset-with-Spirent-and-Cardiff-University/
tags:
  - Electromagnetics
  - Antennas
  - Antenna Arrays
  - Simulation
  - PyVista
  - GNSS
  - Measurements
  
---
Initial mapping of the vehicular Global Navigation Satellite System (GNSS) measurement dataset created with Spirent and Cardiff University.

---
The measurement setup allowed by the generous equipment loan by Spirent, and the help of the Cardiff University included an Ouster OS0-128 Lidar, a Spirent GSS6450 GNSS Signal Recorder, and a Novatel GNSS-850 GPS receiver, allowing us to record a high quality "ground truth" track, together with the L1 band over three cohrent RF channels with a bandwidth of 10MHz, and a sampling resolution at the ADC of 8 bits. This was then combined with my work on spatial modelling using [LyceanEM](https://github.com/LyceanEM/LyceanEM-Python) and `skyfield` to calculate the GPS satellite positions and antenna patterns relative to the local spatial map captured with the Lidar and my three Luxonis Oak-D W cameras.

![Test Setup](/images/20230810_124135.jpg)
Test Setup before mounting on the car.

![Out on the Clifton Downs](/images/20230811_152327.jpg) 
Thanks to my kind collaborators at Cardiff who took a picture of me posing by our test setup.

The weather was glorious, with excellent light for the cameras. I have used `pyvista` to create a merged video stream of the first measurement set through the Clifton Gorge and underneath the famous suspension bridge. 

[Clifton Gorge Video Stream](https://youtu.be/Dr_yOmyhg9Q)

While only initial processing work has been done, I have included a map of the 7 different measurement tracks, from Clifton Downs, through Clifton Gorge, into the Bear Pit in the centre of Bristol, and back again. In addition, a recording was made of the entrance into the underground parking for the Merchant Venturers Building. This dataset will be provided open source with suitable metadata by the end of the year, and we look forward to engaging with other research groups.

There is further information in my poster on the topic for the Operating in the Future Electromagnetic Environment Symposium, which can be found in my [publications](https://lyceanem.com/publication/2023-11-22-Spatial-Modelling-for-GPS-Replication-in-Natural-and-Urban-Canyons).

<iframe src="/files/Satellite_Availability.html" height="800" width="1000"></iframe>

[Direct Link](/files/Satellite_Availability.html)

<script src="https://utteranc.es/client.js"
        repo="LyceanEM/LyceanEM.github.io"
        issue-term="Vehicular-Dataset-with-Spirent-and-University-of-Cardiff"
        theme="github-light"
        crossorigin="anonymous"
        async>
</script>
