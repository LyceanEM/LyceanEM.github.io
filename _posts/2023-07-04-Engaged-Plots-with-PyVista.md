---
title: 'Engaging Plots with PyVista'
date: 2023-07-04
permalink: /posts/2023/07/Engaging-Plots-with-PyVista/
tags:
  - Electromagnetics
  - Antennas
  - Antenna Arrays
  - Simulation
  - PyVista
  
---
An intial exploration of PyVista for interactive 3D plots, and the challenges and opportunities for interactive plots in webpages.


---
```{python}

    import pyvista as pv
    sphere = pv.Sphere()
       
    # long example
    plotter = pv.Plotter(notebook=True)
    plotter.add_mesh(sphere)
    plotter.show(jupyter_backend='trame')
    
```
[](/files/sphererender.html)


<script src="https://utteranc.es/client.js"
        repo="LyceanEM/LyceanEM.github.io"
        issue-term="Engaging-Plots-with-PyVista"
        theme="github-light"
        crossorigin="anonymous"
        async>
</script>
