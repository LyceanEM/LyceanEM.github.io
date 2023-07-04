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
While I haven't been able to embed the visualisations into the page, they are easy to download from the jupyter notebook as html files, which can then be uploaded and linked.

[PyVista](https://docs.pyvista.org/version/stable/) provides some excellent tools for 3d plotting and mesh analysis, and I am looking quite closely at it for new ways of plotting antenna patterns and sources and fields within [LyceanEM](https://documentation.lyceanem.com).

The simplest example is a sphere without data attached.

```{python}

    import pyvista as pv
    sphere = pv.Sphere()
       
    # long example
    plotter = pv.Plotter(notebook=True)
    plotter.add_mesh(sphere)
    plotter.show(jupyter_backend='trame')
    
```
[Sphere](/files/sphererender.html)

While not easy to integrate into my current website setup, it is very easy to export a `PyVista` graph as a mesh, which can then be plotted in `ParaView`, leading to very nice visualisations.

![Beamformed Directivity](/images/UAVBeamformedDirectivityMapVPol.png)

This renders nicely in `Paraview`, but there is no substitute for a live 3D graph.

[Beamformed Directivity](/files/UAVExample.html)

<script src="https://utteranc.es/client.js"
        repo="LyceanEM/LyceanEM.github.io"
        issue-term="Engaging-Plots-with-PyVista"
        theme="github-light"
        crossorigin="anonymous"
        async>
</script>
