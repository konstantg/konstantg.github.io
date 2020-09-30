---
layout: project
comments: false
category: projects
title: Optimizing B-spline surfaces for developability and paneling architectural freeform surfaces
---

<div class="project__authors">
<a href="{{ site.url }}" target="_blank">Konstantinos Gavriil</a>,
<a href="https://www.linkedin.com/in/alexschiftner/" target="_blank">Alexander Schiftner</a>,
<a href="https://www.dmg.tuwien.ac.at/pottmann/" target="_blank">Helmut Pottmann</a>.
</div>

<div class="project__journal">
<span style="font-style: italic;">Computer-Aided Design</span>, <strong>111</strong>, 29-43, 2019.<br>
</div>

<a href="../assets/pdf/bspline_dev.pdf" class="button" target="_blank">
pdf
</a>
<a href="https://doi.org/10.1016/j.cad.2019.01.006" class="button" target="_blank">
doi
</a>
<a href="https://arxiv.org/abs/1808.07560" class="button" target="_blank">
arxiv
</a>



<div class="img_extend">
    <div class="img_container">
        <div id="img_extend">
            <img style="width: 100%;border: 1px solid #272727;" src="../assets/img/projects/bspline_dev/1.png">
            <figcaption>Optimization for developability is done per panel for a panelized surface.</figcaption>
        </div>
    </div>
</div>


# Abstract
<hr>
<p class="project__abstract">
Motivated by applications in architecture and design, we present a novel method for increasing the developability of a B-spline surface. We use the property that the Gauss image of a developable surface is 1-dimensional and can be locally well approximated by circles. This is cast into an algorithm for thinning the Gauss image by increasing the planarity of the Gauss images of appropriate neighborhoods. A variation of the main method allows us to tackle the problem of paneling a freeform architectural surface with developable panels, in particular enforcing rotational cylindrical, rotational conical and planar panels, which are the main preferred types of developable panels in architecture due to the reduced cost of manufacturing.
</p>
<hr>

# Results

<div class="img_extend">
    <div class="img_container">
        <div id="img_extend">
            <img style="width: 100%;" src="../assets/img/projects/bspline_dev/2.png">
            <figcaption>Paneling part of a torus with a different number of cylindrical panels. Both the cutting planes per panel and the inner boundary curves follow the direction of the smaller radius circles that define the torus.</figcaption>
        </div>
    </div>
</div>

<div class="img_extend">
    <div class="img_container">
        <div id="img_extend">
            <img style="width: 100%;border-bottom: 1px solid #ccc;" src="../assets/img/projects/bspline_dev/3a.png">
            <img style="width: 100%;" src="../assets/img/projects/bspline_dev/3b.png">
            <figcaption>Top: the configuration of the deformed leather patch, the mesh acquired from scanning the leather material, and the material’s geometry represented as a B-spline surface. Bottom: the optimized B-spline surface in
solid color compared to the transparent initial surface, the Gauss images of the initial and optimized surfaces.</figcaption>
        </div>
    </div>
</div>

<div class="img_extend">
    <div class="img_container">
        <div id="img_extend" style="position: relative;">
            <img style="width: 100%;" src="../assets/img/projects/bspline_dev/4.png">
            <div style="font-size: 9pt;color: #707070;position: absolute; left: 17%; bottom: 4%;">1</div>
            <div style="font-size: 9pt;color: #707070;position: absolute; left: 89.5%; bottom: 42%;">-4e-7</div>
            <div style="font-size: 9pt;color: #707070;position: absolute; left: 89.5%; bottom: 66%;">&nbsp;4e-7</div>
            <div style="font-size: 9pt;color: #707070;position: absolute; left: 89.5%; bottom: 54%;">&nbsp;&nbsp;&nbsp;&nbsp;0</div>
        </div>
        <figcaption>The Gaussian curvature of the surface for different numbers of optimization iterations, namely at 0, 5, and 15.
</figcaption>
    </div>
</div>

# BibTex
```
@article{Gavriil2019,
author = {Gavriil, Konstantinos and Schiftner, Alexander and Pottmann, Helmut},
title = {Optimizing B-spline surfaces for developability and paneling architectural freeform surfaces},
journal = {Computer-Aided Design},
volume = {111},
pages = {29 - 43},
year = {2019},
issn = {0010-4485},
doi = {10.1016/j.cad.2019.01.006}
}
```


# Acknowledgements
<p class="project__acknowledgements">We would like to thank <a href="http://www.iemar.tuwien.ac.at/?page_id=905" target="_blank">Heinz Schmiedhofer</a> for providing the scan and picture of the leather surface example in Figure 8.
This project has received funding from the European Union’s Horizon 2020 research and innovation programme under the Marie Skłodowska-Curie grant agreement No 675789.</p>
