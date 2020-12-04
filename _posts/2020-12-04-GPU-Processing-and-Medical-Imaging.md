---
title: 'GPU Processing and Medical Imaging'
date: 2020-12-04
permalink: /posts/2020/12/GPU-Processing-and-Medical-Imaging/
tags:
  - LyceanEM
---

Introduction to GPU accelerated processing, and exploration of medical imaging

---
This week I completed moving my EM processing within my latest model from CPU calculation to GPU processing. This is important because it is on the order of 250 times faster, with the efficiency increasing as the problem size increases, due to the GPU being &quot;loaded&quot; more efficiently.

In order to explore this, an interesting example is to model the fields impinging upon an uneven surface from a conformal antenna array, such as might be used for medical imaging. The prospect of convenient microwave medical imaging is one which has long fascinated me.
![Relative Scale](/images/RelativeGainColorbar.png "Relative Power Color scale")

![Head Imaging](/images/medicalimagingneutralfocus.png "Relative Power plotted over Body Model")

![Weighted Head Imaging](/images/medicalimagingformedtohead.png "Relative Power plotted over body Model, weighted towards head")

![Chest Imaging](/images/medicalimagingchestneutralfocus.png "Relative Power plotted over body model, with scanner located over chest region")

![Chest Imaging](/images/medicalimagingchestneutralfocusupright.png "Relative Power plotted over body model, with scanner located over chest region")

<script src="https://utteranc.es/client.js"
        repo="LyceanEM/LyceanEM.github.io"
        issue-term="GPU-Processing-and-Medical-Imaging"
        theme="github-light"
        crossorigin="anonymous"
        async>
</script>
