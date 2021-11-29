---
title: 'Profiling, Electromagnetics and GPU Processing'
date: 2021-06-01
permalink: /posts/2021/06/Profiling-Electromagnetics-and-GPU-Processing/
tags:
  - LyceanEM
---

Discussions of the struggles of electromagnetics development, profiling, and the benefits of the GPU architecture

---

The electromagnetics model I have been working on was implemented using the assumption that an array of ray paths would be loaded onto the GPU, the processing would be done, and an array of the same length would be retrieved and summed according to arrival node by the CPU. This was reliable using my coding skills at the time, but the sorting function was a significant time delay to the model.


<script src="https://utteranc.es/client.js"
        repo="LyceanEM/LyceanEM.github.io"
        issue-term="Profiling-Electromagnetics-and-GPU-Processing"
        theme="github-light"
        crossorigin="anonymous"
        async>
</script>
