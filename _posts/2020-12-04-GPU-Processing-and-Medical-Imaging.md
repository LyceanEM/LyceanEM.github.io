---
title: 'GPU Processing and Medical Imaging'
date: 2020-12-04
permalink: /posts/2020/12/GPU-Processing-and-Medical-Imaging/
tags:
  - LyceanEM
---

Introduction to GPU accelerated processing, and exploration of medical imaging

---
This week I completed moving my electromagnetics processing within my latest model from CPU calculation to GPU processing. This is important because it is on the order of 250 times faster, with the efficiency increasing as the problem size increases, due to the GPU being &quot;loaded&quot; more efficiently.

In order to explore this, an interesting example is to model the fields impinging upon an uneven surface from a conformal antenna array, such as might be used for medical imaging. The prospect of convenient microwave medical imaging is one which has long fascinated me.

In order to explore this, I have created a ring structure with internal radius 0.5m, and width 0.3m. I then populated the internal surface with electric current sources aligned along the x direction, and spaced at intervals of 0.05m, half a wavelength at 3GHz. These are shown as blue arrows inside the green ring structure.

In order to have a model to propagate against, I have created a stand in for a human, with 26756 points across its surface, located in the centroid of each triangle making up the structure of the body model.

![Head Imaging](/images/medicalimagingneutralfocus.png "Relative Power plotted over Body Model")
*Figure 1 Initial Head Imaging*

When the scanner is situated about the head of the body model, the electromagnetic radiation can then be propagated towards the sources in order to model the influence of each individual antenna element or current source upon the total field. For purely line of sight propagation with no scattering assumed, this implies 11.8 million ray checks, and EM processing of a similar number of paths. The power pattern this produces is shown in Figure 1 with each element weighted with zero phase offset.

![Weighted Head Imaging](/images/medicalimagingformedtohead.png "Relative Power plotted over body Model, weighted towards head")
*Figure 2 Equal Gain Combining*

In a naive attempt to manipulate the focus of the scanner, I selected a point on the forehead of the model, and inverted the respective field phase at this point to produce element weights. However, as Figure 2 shows, this does not improve the field distribution over the head, and surprisingly does not even improve the power at the point selected.

![Chest Imaging](/images/medicalimagingchestneutralfocus.png "Relative Power plotted over body model, with scanner located over chest region")
*Figure 3 Chest Imaging*

When the scanner is moved over the chest region, a new power pattern is produced, showing the same type of nodal distribution over the chest. It leads me to consider what sort of distribution would be best for imaging the internal structure of the body, would a focal spot, or some kind of evenly distributed field be appropriate?

![Chest Imaging](/images/medicalimagingchestneutralfocusupright.png "Relative Power plotted over body model, with scanner located over chest region")
*Figure 4 Chest Imaging (Upright)*

The biggest problem in medical imaging, is not the resolution per say, but the dynamic range. The majority of the incident field will be reflected off the skin, while the reflections within the body are attenuated both as they propagate within the body, and out through the skin again.

The most common approach to this problem is to situate the sensing array as close to the skin as possible, with some kind of matching medium between the antenna array and the body part to be imaged.


<script src="https://utteranc.es/client.js"
        repo="LyceanEM/LyceanEM.github.io"
        issue-term="GPU-Processing-and-Medical-Imaging"
        theme="github-light"
        crossorigin="anonymous"
        async>
</script>
