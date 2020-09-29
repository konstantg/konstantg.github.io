---
layout: project
comments: false
category: projects
title: Computational Design of Cold Bent Glass Façades
---

<!-- <div style="font-family: 'Roboto';font-size: 0.8em;">
Konstantinos Gavriil, Ruslan Guseinov, Jesús Pérez, Davide Pellis, Paul Henderson, Florian Rist, Helmut Pottmann, Bernd Bickel.
</div> -->

<div class="project__authors">
<a href="https://konstantg.me/" target="_blank">Konstantinos Gavriil</a>,
<a href="http://ruslanguseinov.com/" target="_blank">Ruslan Guseinov</a>,
<a href="https://sites.google.com/view/jesusprod" target="_blank">Jesús Pérez</a>,
<a href="https://www.geometrie.tuwien.ac.at/pellis/" target="_blank">Davide Pellis</a>,
<a href="https://www.pmh47.net/" target="_blank">Paul Henderson</a>,
<a href="http://e2642.kunst.tuwien.ac.at/index.php?idcatside=11" target="_blank">Florian Rist</a>,
<a href="https://www.dmg.tuwien.ac.at/pottmann/" target="_blank">Helmut Pottmann</a>,
<a href="http://berndbickel.com/about-me/" target="_blank">Bernd Bickel</a>.
</div>

<div class="project__journal">
<span style="font-style: italic;">ACM Transactions on Graphics</span>, <strong>39</strong>(6), 208:1-208:16, 2020. (to appear)<br>
(Proc. ACM SIGGRAPH Asia)
</div>

<a href="../assets/pdf/coldglass.pdf" class="button" target="_blank">
pdf
</a>
<a href="https://doi.org/10.1145/3414685.3417843" class="button" target="_blank">
doi
</a>
<a href="https://arxiv.org/abs/2009.03667" class="button" target="_blank">
arxiv
</a>

<div class="img_extend">
    <div class="img_container">
        <div id="img_extend">
            <img style="width: 100%;" src="/assets/img/projects/coldglass/1.png">
            <figcaption>Rendering of a cold bent glass façade designed with our tool.</figcaption>
        </div>
    </div>
</div>


# Abstract
<hr>
<p class="project__abstract">Cold bent glass is a promising and cost-efficient method for realizing doubly curved glass façades. They are produced by attaching planar glass sheets to curved frames and require keeping the occurring stress within safe limits. However, it is very challenging to navigate the design space of cold bent glass panels due to the fragility of the material, which impedes the form-finding for practically feasible and aesthetically pleasing cold bent glass façades. We propose an interactive, data-driven approach for designing cold bent glass façades that can be seamlessly integrated into a typical architectural design pipeline. Our method allows non-expert users to interactively edit a parametric surface while providing real-time feedback on the deformed shape and maximum stress of cold bent glass panels. Designs are automatically refined to minimize several fairness criteria while maximal stresses are kept within glass limits. We achieve interactive frame rates by using a differentiable Mixture Density Network trained from more than a million simulations. Given a curved boundary, our regression model is capable of handling multistable configurations and accurately predicting the equilibrium shape of the panel and its corresponding maximal stress. We show predictions are highly accurate and validate our results with a physical realization of a cold bent glass surface.</p>
<hr>

# Results
<div class="img_extend">
    <div class="img_container">
        <div id="img_extend">
            <img style="width: 100%;" src="/assets/img/projects/coldglass/2.jpg">
            <figcaption> Material-aware form finding of a cold bent glass façade.
            From left to right: initial and revised panel layouts from an interactive design session with immediate feedback on the glass shape and maximum stress (red color indicates panel failure).
            The surface design is then optimized for stress reduction and smoothness.
            The final façade realization using cold bent glass features doubly curved areas and smooth reflections.</figcaption>
        </div>
    </div>
</div>

<div class="img_extend">
    <div class="img_container">
        <div id="img_extend">
            <img style="width: 100%;" src="/assets/img/projects/coldglass/3.gif">
            <figcaption>Interactive session with our design tool, which was integrated to Rhino.
            The tool provides real-time predictions for the panel shape in the form of cubic Bézier surfaces, and for the maximal stress of the panel; here color-coded as safe (blue), critical (pink), and breaking (red).
            Yellow panels are ignored as their shape is outside the prediction domain of the model.</figcaption>
        </div>
    </div>
</div>

<div class="img_extend">
    <div class="img_container">
        <div id="img_extend">
            <img style="width: 100%;" src="/assets/img/projects/coldglass/4.jpg">
            <figcaption>Dominant cold bent glass realizations of the NHHQ design, the Lilium Tower, and another double-curved architectural design.</figcaption>
        </div>
    </div>
</div>

<div class="img_extend">
    <div class="img_container">
        <div id="img_extend">
            <img style="width: 100%;" src="/assets/img/projects/coldglass/5.jpg">
            <figcaption> Realization of a double-curved surface using 3×3 cold bent panels.</figcaption>
        </div>
    </div>
</div>

# Video
<div class="img_extend">
    <div class="img_container">
        <div id="img_extend">
          <div style="position: relative;width: 100%;height: 0;padding-bottom: 56.25%;">
            <iframe src="https://www.youtube.com/embed/FStBxKC4GkQ?color=white&modestbranding=1&autohide=1&showinfo=0&iv_load_policy=3&rel=0" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position:absolute;top: 0;left: 0;width: 100%;height: 100%;"></iframe>
          </div>
        </div>
    </div>
</div>

# BibTex
```
@article{Gavriil2020,
author = {Gavriil, Konstantinos and Guseinov, Ruslan and P{\'e}rez, Jes{\'u}s and Pellis, Davide and Henderson, Paul and Rist, Florian and Pottmann, Helmut and Bickel, Bernd},
title = {Computational Design of Cold Bent Glass Fa{\c c}ades},
journal = {ACM Transactions on Graphics (SIGGRAPH Asia 2020)},
year = {2020},
month = {12},
volume = {39},
number = {6}
articleno = {208},
numpages = {16}
}
```


# Acknowledgements
<p class="project__acknowledgements">We thank IST Austria’s Scientific Computing team for their support, Corinna Datsiou and Sophie Pennetier for their expert input on the practical applications of cold bent glass, and Zaha Hadid Architects and Waagner Biro for providing the architectural datasets. This project has received funding from the European Union’s Horizon 2020 research and innovation program under grant agreement No 675789 - Algebraic Representations in Computer-Aided Design for complEx Shapes (ARCADES), from the European Research Council (ERC) under grant agreement No 715767 - MATERIALIZABLE: Intelligent fabrication-oriented Computational Design and Modeling, and SFB-Transregio “Discretization in Geometry and Dynamics” through grant I 2978 of the Austrian Science Fund (FWF). F. Rist and K. Gavriil have been partially supported by KAUST baseline funding.</p>
