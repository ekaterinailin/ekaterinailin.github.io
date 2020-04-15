---
layout: post
title: "TEST"
excerpt: "TEST2
"
categories: [ASTRONOMY]
author: ekaterina
comments: true
---
<html>
<head><meta charset="utf-8" />


<title>Test</title>

 <style type="text/css">
        /* Temporary definitions which will become obsolete with Notebook release 5.0 */
        .ansi-black-fg {
            color: #3E424D;
        }

        .ansi-black-bg {
            background-color: #3E424D;
        }

        .ansi-black-intense-fg {
            color: #282C36;
        }

        .ansi-black-intense-bg {
            background-color: #282C36;
        }

        .ansi-red-fg {
            color: #E75C58;
        }

        .ansi-red-bg {
            background-color: #E75C58;
        }

        .ansi-red-intense-fg {
            color: #B22B31;
        }

        .ansi-red-intense-bg {
            background-color: #B22B31;
        }

        .ansi-green-fg {
            color: #00A250;
        }

        .ansi-green-bg {
            background-color: #00A250;
        }

        .ansi-green-intense-fg {
            color: #007427;
        }

        .ansi-green-intense-bg {
            background-color: #007427;
        }

        .ansi-yellow-fg {
            color: #DDB62B;
        }

        .ansi-yellow-bg {
            background-color: #DDB62B;
        }

        .ansi-yellow-intense-fg {
            color: #B27D12;
        }

        .ansi-yellow-intense-bg {
            background-color: #B27D12;
        }

        .ansi-blue-fg {
            color: #208FFB;
        }

        .ansi-blue-bg {
            background-color: #208FFB;
        }

        .ansi-blue-intense-fg {
            color: #0065CA;
        }

        .ansi-blue-intense-bg {
            background-color: #0065CA;
        }

        .ansi-magenta-fg {
            color: #D160C4;
        }

        .ansi-magenta-bg {
            background-color: #D160C4;
        }

        .ansi-magenta-intense-fg {
            color: #A03196;
        }

        .ansi-magenta-intense-bg {
            background-color: #A03196;
        }

        .ansi-cyan-fg {
            color: #60C6C8;
        }

        .ansi-cyan-bg {
            background-color: #60C6C8;
        }

        .ansi-cyan-intense-fg {
            color: #258F8F;
        }

        .ansi-cyan-intense-bg {
            background-color: #258F8F;
        }

        .ansi-white-fg {
            color: #C5C1B4;
        }

        .ansi-white-bg {
            background-color: #C5C1B4;
        }

        .ansi-white-intense-fg {
            color: #A1A6B2;
        }

        .ansi-white-intense-bg {
            background-color: #A1A6B2;
        }

        .ansi-bold {
            font-weight: bold;
        }
    </style>

<!-- Loading mathjax macro -->
<!-- Load mathjax -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.5/latest.js?config=TeX-AMS_HTML"></script>
    <!-- MathJax configuration -->
    <script type="text/x-mathjax-config">
    MathJax.Hub.Config({
        tex2jax: {
            inlineMath: [ ['$','$'], ["\\(","\\)"] ],
            displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
            processEscapes: true,
            processEnvironments: true
        },
        // Center justify equations in code and markdown cells. Elsewhere
        // we use CSS to left justify single line equations in code cells.
        displayAlign: 'center',
        "HTML-CSS": {
            styles: {'.MathJax_Display': {"margin": 0}},
            linebreaks: { automatic: true }
        }
    });
    </script>
    <!-- End of mathjax configuration -->

<style>
        .cell.nbinteract-left {
            width: 50%;
            float: left;
        }

        .cell.nbinteract-right {
            width: 50%;
            float: right;
        }

        .cell.nbinteract-hide_in > .input {
            display: none;
        }

        .cell.nbinteract-hide_out > .output_wrapper {
            display: none;
        }

        .cell:after {
          content: "";
          display: table;
          clear: both;
        }

        div.output_subarea {
            max-width: initial;
        }

        .jp-OutputPrompt {
            display: none;
        }
    </style></head>
<body>
  <div tabindex="-1" id="notebook" class="border-box-sizing">
    <div class="container">
      



  <div class="cell text_cell">
    <button class="js-nbinteract-widget">
      Loading widgets...
    </button>
  </div>




  

  <div class="
      cell border-box-sizing code_cell rendered">
    <div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Basic packages</span>
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="kn">import</span> <span class="nn">pandas</span> <span class="k">as</span> <span class="nn">pd</span>

<span class="c1"># Get astronomical units</span>
<span class="kn">import</span> <span class="nn">astropy.units</span> <span class="k">as</span> <span class="nn">u</span> 

<span class="c1"># Used for nice interactive widgets</span>
<span class="kn">from</span> <span class="nn">ipywidgets</span> <span class="kn">import</span> <span class="n">interact</span><span class="p">,</span> <span class="n">FloatSlider</span>
<span class="kn">from</span> <span class="nn">IPython.display</span> <span class="kn">import</span> <span class="n">Markdown</span> <span class="k">as</span> <span class="n">md</span>

<span class="c1"># Used to display the sketch in 1.</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>

<span class="c1"># Define constants for this exercise</span>
<span class="n">vsun</span> <span class="o">=</span> <span class="mf">220.</span> <span class="c1"># km/s  - Sun&#39;s velocity around the Galactic center</span>
</pre></div>

    </div>
</div>
</div>

  </div>
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="1.-Interstellar-cloud">1. Interstellar cloud<a class="anchor-link" href="#1.-Interstellar-cloud">&#182;</a></h1><p>In 21cm observations, you can find many interstellar clouds in the Galactic plane in the direction of $l = 45^o$. The cloud with the largest radial velocity has $v_r = 73\,$km$\,$s$^{-1}$.</p>
<h2 id="What-is-its-distance-from-us?-How-far-is-it-from-the-Galactic-centre?">What is its distance from us? How far is it from the Galactic centre?<a class="anchor-link" href="#What-is-its-distance-from-us?-How-far-is-it-from-the-Galactic-centre?">&#182;</a></h2>
</div>
</div>
</div>

  

   <div class="nbinteract-hide_in
      cell border-box-sizing code_cell rendered">
    <div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">matplotlib.image</span> <span class="k">as</span> <span class="nn">mpimg</span>
<span class="n">img</span> <span class="o">=</span> <span class="n">mpimg</span><span class="o">.</span><span class="n">imread</span><span class="p">(</span><span class="s1">&#39;sketch.png&#39;</span><span class="p">)</span>

<span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">(</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">10</span><span class="p">,</span><span class="mi">10</span><span class="p">))</span>
<span class="n">plt</span><span class="o">.</span><span class="n">axis</span><span class="p">(</span><span class="s2">&quot;off&quot;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">imshow</span><span class="p">(</span><span class="n">img</span><span class="p">);</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    



<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

  </div>
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Figure 1: Schematic view of Sun, interstellar cloud and Galactic centre. Both orange angles are $45^o$.</p>
<p>$R_0$ is the distance from the Sun to the Galactic center. The value varies depending on the method you use to measure it (<a href="https://en.wikipedia.org/wiki/Galactic_Center">Wikipedia: Galactic Center</a>). We adopt $8.2\,$kpc here.</p>
<p>$l$ is given in the exercise.</p>
<p>$D = R = R_0 \cdot \sin l$</p>

</div>
</div>
</div>

  

  <div class="
      cell border-box-sizing code_cell rendered">
    <div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">distance</span><span class="p">(</span><span class="n">R_0</span><span class="p">,</span> <span class="n">l</span><span class="o">=</span><span class="mf">45.</span><span class="p">):</span>
    <span class="sd">&quot;&quot;&quot;Calculate the distance of a cloud</span>
<span class="sd">    to the Sun and the Galactic center if</span>
<span class="sd">    the cloud is tangetially moving right</span>
<span class="sd">    towards us.</span>
<span class="sd">    </span>
<span class="sd">    </span>
<span class="sd">    Parameters:</span>
<span class="sd">    -----------</span>
<span class="sd">    R_0 : float</span>
<span class="sd">        distance from the Sun to the</span>
<span class="sd">        Galactic center</span>
<span class="sd">    l : float</span>
<span class="sd">        angle between the cloud and the</span>
<span class="sd">        Galactic center as seen from the </span>
<span class="sd">        Sun</span>

<span class="sd">    Return:</span>
<span class="sd">    -------</span>
<span class="sd">    string with the distances of the cloud</span>
<span class="sd">    relative to the Sun and the Galactic center</span>
<span class="sd">    &quot;&quot;&quot;</span>
    <span class="n">from_us</span> <span class="o">=</span> <span class="n">R_0</span> <span class="o">*</span> <span class="n">np</span><span class="o">.</span><span class="n">sin</span><span class="p">((</span><span class="n">l</span><span class="o">*</span><span class="n">u</span><span class="o">.</span><span class="n">deg</span><span class="p">)</span><span class="o">.</span><span class="n">to</span><span class="p">(</span><span class="n">u</span><span class="o">.</span><span class="n">rad</span><span class="p">)</span><span class="o">.</span><span class="n">value</span><span class="p">)</span>
    <span class="n">from_center</span> <span class="o">=</span> <span class="n">R_0</span> <span class="o">*</span> <span class="n">np</span><span class="o">.</span><span class="n">cos</span><span class="p">((</span><span class="n">l</span><span class="o">*</span><span class="n">u</span><span class="o">.</span><span class="n">deg</span><span class="p">)</span><span class="o">.</span><span class="n">to</span><span class="p">(</span><span class="n">u</span><span class="o">.</span><span class="n">rad</span><span class="p">)</span><span class="o">.</span><span class="n">value</span><span class="p">)</span>
    <span class="k">return</span> <span class="sa">f</span><span class="s2">&quot;The cloud is </span><span class="si">{</span><span class="n">from_us</span><span class="si">:</span><span class="s2">.2f</span><span class="si">}</span><span class="s2"> kpc away from the Sun, &quot;</span> \
           <span class="sa">f</span><span class="s2">&quot;and </span><span class="si">{</span><span class="n">from_center</span><span class="si">:</span><span class="s2">.2f</span><span class="si">}</span><span class="s2"> kpc away from the Galactic center.&quot;</span>
</pre></div>

    </div>
</div>
</div>

  </div>

  

 <div class="nbinteract-hide_in
      cell border-box-sizing code_cell rendered">
    <div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">x_widget</span> <span class="o">=</span> <span class="n">FloatSlider</span><span class="p">(</span><span class="nb">min</span><span class="o">=</span><span class="mf">7.4</span><span class="p">,</span> <span class="nb">max</span><span class="o">=</span><span class="mf">8.7</span><span class="p">,</span> <span class="n">step</span><span class="o">=</span><span class="mf">0.05</span><span class="p">,</span> <span class="n">description</span><span class="o">=</span><span class="sa">r</span><span class="s2">&quot;$R_0 [kpc]$&quot;</span><span class="p">)</span>
<span class="n">y_widget</span> <span class="o">=</span> <span class="n">FloatSlider</span><span class="p">(</span><span class="nb">min</span><span class="o">=</span><span class="mf">0.</span><span class="p">,</span> <span class="nb">max</span><span class="o">=</span><span class="mf">90.</span><span class="p">,</span> <span class="n">step</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span> <span class="n">value</span><span class="o">=</span><span class="mf">45.</span><span class="p">,</span> <span class="n">description</span><span class="o">=</span><span class="sa">r</span><span class="s2">&quot;$l$ [deg]&quot;</span><span class="p">)</span>

<span class="n">interact</span><span class="p">(</span><span class="n">distance</span><span class="p">,</span> <span class="n">R_0</span><span class="o">=</span><span class="n">x_widget</span><span class="p">,</span> <span class="n">l</span><span class="o">=</span><span class="n">y_widget</span><span class="p">);</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    



  <div class="output_subarea output_widget_view ">
    <button class="js-nbinteract-widget">
      Loading widgets...
    </button>
  </div>

</div>

</div>
</div>

  </div>
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Calculate-the-velocity-with-which-the-star-is-rotating-around-the-Galactic-center.">Calculate the velocity with which the star is rotating around the Galactic center.<a class="anchor-link" href="#Calculate-the-velocity-with-which-the-star-is-rotating-around-the-Galactic-center.">&#182;</a></h2><p>Transform the following relation</p>
<p>$v_r = R_{0}(\frac{v_*}{R} - \frac{v_{\odot}}{R_{0}})\sin l $</p>
<p>to</p>
<p>$v_* = (\frac{v_r}{R_{0}\sin l} + \frac{v_{\odot}}{R_{0}})R $</p>
<p>and plug in the numbers:</p>

</div>
</div>
</div>

  

  <div class="
      cell border-box-sizing code_cell rendered">
    <div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">velocity</span><span class="p">(</span><span class="n">R_0</span><span class="p">,</span> <span class="n">l</span><span class="p">,</span> <span class="n">vr</span><span class="p">):</span>
    <span class="sd">&quot;&quot;&quot;Calculate the velocity with </span>
<span class="sd">    which the cloud is rotating around </span>
<span class="sd">    the Galactic center.</span>
<span class="sd">    </span>
<span class="sd">    Parameters:</span>
<span class="sd">    -----------</span>
<span class="sd">    R_0 : float</span>
<span class="sd">        distance from the Sun to the</span>
<span class="sd">        Galactic center</span>
<span class="sd">    l : float</span>
<span class="sd">        angle between the cloud and the</span>
<span class="sd">        Galactic center as seen from the </span>
<span class="sd">        Sun in degrees</span>
<span class="sd">    vr : float</span>
<span class="sd">        radial velocity of the cloud in km/s</span>
<span class="sd">        </span>
<span class="sd">    Return:</span>
<span class="sd">    -------</span>
<span class="sd">    string with the value for the cloud&#39;s</span>
<span class="sd">    rotation velocity</span>
<span class="sd">    &quot;&quot;&quot;</span>
    <span class="n">R</span> <span class="o">=</span> <span class="n">R_0</span> <span class="o">*</span> <span class="n">np</span><span class="o">.</span><span class="n">sin</span><span class="p">((</span><span class="n">l</span><span class="o">*</span><span class="n">u</span><span class="o">.</span><span class="n">deg</span><span class="p">)</span><span class="o">.</span><span class="n">to</span><span class="p">(</span><span class="n">u</span><span class="o">.</span><span class="n">rad</span><span class="p">)</span><span class="o">.</span><span class="n">value</span><span class="p">)</span>
    <span class="n">vr</span> <span class="o">=</span> <span class="n">R</span> <span class="o">*</span> <span class="p">(</span><span class="n">vr</span> <span class="o">/</span> <span class="n">R</span> <span class="o">+</span> <span class="n">vsun</span> <span class="o">/</span> <span class="n">R_0</span><span class="p">)</span>
    
    <span class="k">return</span> <span class="sa">f</span><span class="s2">&quot;The cloud is rotating at </span><span class="si">{</span><span class="n">vr</span><span class="si">:</span><span class="s2">.2f</span><span class="si">}</span><span class="s2"> km/s.&quot;</span>
</pre></div>

    </div>
</div>
</div>

  </div>

  

 <div class="nbinteract-hide_in
      cell border-box-sizing code_cell rendered">
    <div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">x_widget</span> <span class="o">=</span> <span class="n">FloatSlider</span><span class="p">(</span><span class="nb">min</span><span class="o">=</span><span class="mf">7.4</span><span class="p">,</span> <span class="nb">max</span><span class="o">=</span><span class="mf">8.7</span><span class="p">,</span> <span class="n">step</span><span class="o">=</span><span class="mf">0.05</span><span class="p">,</span> <span class="n">description</span><span class="o">=</span><span class="sa">r</span><span class="s2">&quot;$R_0$ [kpc]&quot;</span><span class="p">)</span>
<span class="n">y_widget</span> <span class="o">=</span> <span class="n">FloatSlider</span><span class="p">(</span><span class="nb">min</span><span class="o">=</span><span class="mf">0.</span><span class="p">,</span> <span class="nb">max</span><span class="o">=</span><span class="mf">90.</span><span class="p">,</span> <span class="n">step</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span> <span class="n">value</span><span class="o">=</span><span class="mf">45.</span><span class="p">,</span> <span class="n">description</span><span class="o">=</span><span class="sa">r</span><span class="s2">&quot;$l$ [deg]&quot;</span><span class="p">)</span>
<span class="n">z_widget</span> <span class="o">=</span> <span class="n">FloatSlider</span><span class="p">(</span><span class="nb">min</span><span class="o">=</span><span class="mf">0.</span><span class="p">,</span> <span class="nb">max</span><span class="o">=</span><span class="mf">200.</span><span class="p">,</span> <span class="n">step</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span> <span class="n">value</span><span class="o">=</span><span class="mf">73.</span><span class="p">,</span> <span class="n">description</span><span class="o">=</span><span class="sa">r</span><span class="s2">&quot;$v$ [km/s]&quot;</span><span class="p">)</span>

<span class="n">interact</span><span class="p">(</span><span class="n">velocity</span><span class="p">,</span> <span class="n">R_0</span><span class="o">=</span><span class="n">x_widget</span><span class="p">,</span> <span class="n">l</span><span class="o">=</span><span class="n">y_widget</span><span class="p">,</span> <span class="n">vr</span><span class="o">=</span><span class="n">z_widget</span><span class="p">);</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    



  <div class="output_subarea output_widget_view ">
    <button class="js-nbinteract-widget">
      Loading widgets...
    </button>
  </div>

</div>

</div>
</div>

  </div>
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="How-many-orbits-around-the-Galactic-centre-did-the-cloud-complete-in-one-Galactic-year-(the-time-it-takes-the-Sun-to-orbit-the-Galactic-centre-once)?">How many orbits around the Galactic centre did the cloud complete in one Galactic year (the time it takes the Sun to orbit the Galactic centre once)?<a class="anchor-link" href="#How-many-orbits-around-the-Galactic-centre-did-the-cloud-complete-in-one-Galactic-year-(the-time-it-takes-the-Sun-to-orbit-the-Galactic-centre-once)?">&#182;</a></h2><p>For the Sun, the time $T_{\odot}$ it takes to complete one orbit around the Galactic centre is:</p>
<p>$T_{\odot} = \dfrac{2 \pi R_0}{v_{\odot}}$</p>
<p>In this time, the cloud can travel:</p>
<p>$\Delta d_{cloud} = \dfrac{v_{cloud} T_{\odot}}{2 \pi R} = \dfrac{v_{cloud} R_0 }{v_0  R}$</p>
<p>in units of full rotations of the cloud around the Galactic center.</p>

</div>
</div>
</div>

  

  <div class="
      cell border-box-sizing code_cell rendered">
    <div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">rotations_around_galactic_center</span><span class="p">(</span><span class="n">R_0</span><span class="p">,</span> <span class="n">v_cloud</span><span class="p">,</span> <span class="n">R</span><span class="p">):</span>
    <span class="sd">&quot;&quot;&quot; Formula for d_cloud.</span>
<span class="sd">    </span>
<span class="sd">    Parameters:</span>
<span class="sd">    -----------</span>
<span class="sd">    R_0 : float</span>
<span class="sd">        distance from the Sun to the</span>
<span class="sd">        Galactic center in kpc</span>
<span class="sd">    v_cloud : float</span>
<span class="sd">        the clouds velocity on the</span>
<span class="sd">        orbit around the Galactic center</span>
<span class="sd">    R : float</span>
<span class="sd">        distance from the cloud to the</span>
<span class="sd">        Galactic center</span>
<span class="sd">    </span>
<span class="sd">    Return:</span>
<span class="sd">    -------</span>
<span class="sd">    string with the number of rotations    </span>
<span class="sd">    &quot;&quot;&quot;</span>
    <span class="n">dcloud</span> <span class="o">=</span> <span class="n">v_cloud</span> <span class="o">*</span> <span class="p">(</span><span class="n">R_0</span> <span class="o">*</span> <span class="n">u</span><span class="o">.</span><span class="n">kpc</span><span class="p">)</span><span class="o">.</span><span class="n">to</span><span class="p">(</span><span class="n">u</span><span class="o">.</span><span class="n">km</span><span class="p">)</span> <span class="o">/</span> <span class="n">vsun</span> <span class="o">/</span> <span class="p">(</span><span class="n">R</span> <span class="o">*</span> <span class="n">u</span><span class="o">.</span><span class="n">kpc</span><span class="p">)</span><span class="o">.</span><span class="n">to</span><span class="p">(</span><span class="n">u</span><span class="o">.</span><span class="n">km</span><span class="p">)</span>
    <span class="k">return</span> <span class="n">md</span><span class="p">(</span><span class="sa">f</span><span class="s2">&quot;$\Delta d_</span><span class="se">{{</span><span class="s2">cloud</span><span class="se">}}</span><span class="s2">=</span><span class="si">{</span><span class="n">dcloud</span><span class="si">:</span><span class="s2">.2f</span><span class="si">}</span><span class="s2">$ rotations around the Galactic center.&quot;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

  </div>

  

  <div class="
      cell border-box-sizing code_cell rendered">
    <div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">ws_widget</span> <span class="o">=</span> <span class="n">FloatSlider</span><span class="p">(</span><span class="nb">min</span><span class="o">=</span><span class="mf">0.</span><span class="p">,</span> <span class="nb">max</span><span class="o">=</span><span class="mf">400.</span><span class="p">,</span> <span class="n">step</span><span class="o">=</span><span class="mi">5</span><span class="p">,</span> <span class="n">value</span><span class="o">=</span><span class="mf">228.</span><span class="p">,</span> <span class="n">description</span><span class="o">=</span><span class="sa">r</span><span class="s2">&quot;$v_</span><span class="si">{cloud}</span><span class="s2">$ [km/s]&quot;</span><span class="p">)</span>
<span class="n">r_widget</span> <span class="o">=</span> <span class="n">FloatSlider</span><span class="p">(</span><span class="nb">min</span><span class="o">=</span><span class="mi">0</span><span class="p">,</span> <span class="nb">max</span><span class="o">=</span><span class="mi">15</span><span class="p">,</span> <span class="n">step</span><span class="o">=.</span><span class="mi">1</span><span class="p">,</span> <span class="n">value</span><span class="o">=</span><span class="mf">5.8</span><span class="p">,</span> <span class="n">description</span><span class="o">=</span><span class="sa">r</span><span class="s2">&quot;$R [kpc]$&quot;</span><span class="p">)</span>

<span class="n">interact</span><span class="p">(</span><span class="n">rotations_around_galactic_center</span><span class="p">,</span> <span class="n">R_0</span><span class="o">=</span><span class="n">x_widget</span><span class="p">,</span> <span class="n">v_cloud</span><span class="o">=</span><span class="n">ws_widget</span><span class="p">,</span> <span class="n">R</span><span class="o">=</span><span class="n">r_widget</span><span class="p">);</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    



  <div class="output_subarea output_widget_view ">
    <button class="js-nbinteract-widget">
      Loading widgets...
    </button>
  </div>

</div>

</div>
</div>

  </div>
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="2.-Distance-determination-with-Cepheids">2. Distance determination with Cepheids<a class="anchor-link" href="#2.-Distance-determination-with-Cepheids">&#182;</a></h1><p>For three Galactic Cepheids, the parallax $\pi$ (<code>pi_mas</code>, in milliarcseconds), period $P$ (<code>P_d</code>, in days), V-band magnitude $m_V$ (<code>m_V</code>) and interstellar extinction $A_V$ (<code>A_V</code>) were measured:</p>

</div>
</div>
</div>

  

  <div class="
      cell border-box-sizing code_cell rendered">
    <div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">ext</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">({</span><span class="s2">&quot;star&quot;</span><span class="p">:[</span><span class="s2">&quot;RT Aur&quot;</span><span class="p">,</span><span class="s2">&quot;X Sgr&quot;</span><span class="p">,</span> <span class="s2">&quot;l Car&quot;</span><span class="p">],</span>
              <span class="s2">&quot;pi_mas&quot;</span><span class="p">:[</span><span class="mf">2.4</span><span class="p">,</span><span class="mf">3.</span><span class="p">,</span><span class="mf">2.01</span><span class="p">],</span>
              <span class="s2">&quot;P_d&quot;</span><span class="p">:[</span><span class="mf">3.728190</span><span class="p">,</span> <span class="mf">7.012877</span><span class="p">,</span> <span class="mf">35.551341</span><span class="p">],</span>
              <span class="s2">&quot;m_V&quot;</span><span class="p">:[</span><span class="mf">5.464</span><span class="p">,</span> <span class="mf">4.556</span><span class="p">,</span> <span class="mf">3.732</span><span class="p">],</span>
              <span class="s2">&quot;A_V&quot;</span><span class="p">:[</span><span class="o">.</span><span class="mi">2</span><span class="p">,</span><span class="o">.</span><span class="mi">58</span><span class="p">,</span><span class="o">.</span><span class="mi">52</span><span class="p">]})</span>
<span class="n">ext</span> <span class="o">=</span> <span class="n">ext</span><span class="o">.</span><span class="n">set_index</span><span class="p">(</span><span class="s2">&quot;star&quot;</span><span class="p">)</span>
<span class="n">ext</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">index</span><span class="o">=</span><span class="nb">str</span><span class="p">,</span> <span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="s2">&quot;pi_mas&quot;</span><span class="p">:</span><span class="sa">r</span><span class="s2">&quot;$\pi$ [mas]&quot;</span><span class="p">,</span>
                               <span class="s2">&quot;P_d&quot;</span><span class="p">:</span><span class="sa">r</span><span class="s2">&quot;$P$ [d]&quot;</span><span class="p">,</span>
                               <span class="s2">&quot;m_V&quot;</span><span class="p">:</span><span class="sa">r</span><span class="s2">&quot;$m_V$&quot;</span><span class="p">,</span>
                               <span class="s2">&quot;A_V&quot;</span><span class="p">:</span><span class="sa">r</span><span class="s2">&quot;$A_V$&quot;</span><span class="p">,})</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    


<div class="output_html rendered_html output_subarea output_execute_result">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>$\pi$ [mas]</th>
      <th>$P$ [d]</th>
      <th>$m_V$</th>
      <th>$A_V$</th>
    </tr>
    <tr>
      <th>star</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>RT Aur</th>
      <td>2.40</td>
      <td>3.728190</td>
      <td>5.464</td>
      <td>0.20</td>
    </tr>
    <tr>
      <th>X Sgr</th>
      <td>3.00</td>
      <td>7.012877</td>
      <td>4.556</td>
      <td>0.58</td>
    </tr>
    <tr>
      <th>l Car</th>
      <td>2.01</td>
      <td>35.551341</td>
      <td>3.732</td>
      <td>0.52</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>
</div>

  </div>
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Find-the-period-luminosity-relation-from-these-measurements.">Find the period-luminosity relation from these measurements.<a class="anchor-link" href="#Find-the-period-luminosity-relation-from-these-measurements.">&#182;</a></h2><p>The general form is:</p>
<p>$M_V = a + b \cdot log P$</p>
<p>Distances to the three stars can be calculated from the given parallaxes and by using the Taylor expansion of the parallax formula:</p>
<p>$D = \left(\frac{p}{1^{\prime\prime}}\right)^{-1}\,\text{pc}$</p>
<p>These distances can then be used in the formula for the distance modulus:</p>
<p>$m - M = 5\log(D/1\,\text{pc}) - 5 + A$</p>
<p>This can be rewritten as:</p>
<p>$ M_V = m_v - 5\log(D/1\,\text{pc}) + 5 - A_V$</p>
<p>This gives the following numbers:</p>
<p>Table 1.</p>

</div>
</div>
</div>

  

  <div class="
      cell border-box-sizing code_cell rendered">
    <div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">ext</span><span class="p">[</span><span class="s2">&quot;D_pc&quot;</span><span class="p">]</span> <span class="o">=</span> <span class="n">ext</span><span class="o">.</span><span class="n">pi_mas</span><span class="o">.</span><span class="n">apply</span><span class="p">(</span><span class="k">lambda</span> <span class="n">x</span><span class="p">:</span> <span class="mf">1.</span><span class="o">*</span><span class="n">u</span><span class="o">.</span><span class="n">arcsec</span> <span class="o">/</span> <span class="p">(</span><span class="n">x</span><span class="o">*</span><span class="n">u</span><span class="o">.</span><span class="n">mas</span><span class="p">)</span><span class="o">.</span><span class="n">to</span><span class="p">(</span><span class="n">u</span><span class="o">.</span><span class="n">arcsec</span><span class="p">))</span>
<span class="n">ext</span><span class="p">[</span><span class="s2">&quot;M_V&quot;</span><span class="p">]</span> <span class="o">=</span> <span class="n">ext</span><span class="o">.</span><span class="n">apply</span><span class="p">(</span><span class="k">lambda</span> <span class="n">x</span><span class="p">:</span> <span class="n">x</span><span class="o">.</span><span class="n">m_V</span> <span class="o">-</span>  <span class="mf">5.</span> <span class="o">*</span> <span class="n">np</span><span class="o">.</span><span class="n">log10</span><span class="p">(</span><span class="n">x</span><span class="o">.</span><span class="n">D_pc</span><span class="p">)</span> <span class="o">+</span> <span class="mf">5.</span> <span class="o">-</span> <span class="n">x</span><span class="o">.</span><span class="n">A_V</span><span class="p">,</span> <span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span>
<span class="n">ext</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    


<div class="output_html rendered_html output_subarea output_execute_result">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>pi_mas</th>
      <th>P_d</th>
      <th>m_V</th>
      <th>A_V</th>
      <th>D_pc</th>
      <th>M_V</th>
    </tr>
    <tr>
      <th>star</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>RT Aur</th>
      <td>2.40</td>
      <td>3.728190</td>
      <td>5.464</td>
      <td>0.20</td>
      <td>416.6666666666667</td>
      <td>-2.8349437914419697</td>
    </tr>
    <tr>
      <th>X Sgr</th>
      <td>3.00</td>
      <td>7.012877</td>
      <td>4.556</td>
      <td>0.58</td>
      <td>333.3333333333333</td>
      <td>-3.638393726401686</td>
    </tr>
    <tr>
      <th>l Car</th>
      <td>2.01</td>
      <td>35.551341</td>
      <td>3.732</td>
      <td>0.52</td>
      <td>497.51243781094536</td>
      <td>-5.272019712897556</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>
</div>

  </div>
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>There are several ways to determine the coefficients $a$ and $b$. One of them is to plot $M_V$ against $\log P$, draw a line through the points by eye and calculate the slope and point where it crossed the y-axis. Doing that you assume that the relationship between both quantities is linear. If this assumption is true, you can use lienar regression to determine the coefficients.</p>
<p>The formulas for linear regression are:</p>
<p>$b = \frac{\sum_i\left(x_i -\overline{x}\right)\left(y_i -\overline{y}\right)}{\sum_i\left(x_i -\overline{x}\right)^2} \qquad\text{and}\quad a = \overline{y} - b\,\overline{x}$</p>
<p>Here, $y = M_V$ and $x = \log P$. $\overline{y}$ and $\overline{x}$ are their average values.</p>

</div>
</div>
</div>

  

  <div class="
      cell border-box-sizing code_cell rendered">
    <div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">linreg_b</span><span class="p">(</span><span class="n">x</span><span class="p">,</span><span class="n">y</span><span class="p">):</span>
    <span class="sd">&quot;&quot;&quot;Linear regression formula for b.&quot;&quot;&quot;</span>
    <span class="n">xmean</span><span class="p">,</span> <span class="n">ymean</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">mean</span><span class="p">(</span><span class="n">x</span><span class="p">),</span> <span class="n">np</span><span class="o">.</span><span class="n">mean</span><span class="p">(</span><span class="n">y</span><span class="p">)</span>
    <span class="k">return</span> <span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">sum</span><span class="p">((</span><span class="n">x</span> <span class="o">-</span> <span class="n">xmean</span><span class="p">)</span> <span class="o">*</span> <span class="p">(</span><span class="n">y</span> <span class="o">-</span> <span class="n">ymean</span><span class="p">))</span> <span class="o">/</span> 
            <span class="n">np</span><span class="o">.</span><span class="n">sum</span><span class="p">((</span><span class="n">x</span> <span class="o">-</span> <span class="n">xmean</span><span class="p">)</span><span class="o">**</span><span class="mi">2</span><span class="p">))</span>

<span class="k">def</span> <span class="nf">linreg_a</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">y</span><span class="p">,</span> <span class="n">b</span><span class="p">):</span>
    <span class="sd">&quot;&quot;&quot;Linear regression formula for a.&quot;&quot;&quot;</span>
    <span class="k">return</span> <span class="n">np</span><span class="o">.</span><span class="n">mean</span><span class="p">(</span><span class="n">y</span><span class="p">)</span> <span class="o">-</span> <span class="n">b</span> <span class="o">*</span> <span class="n">np</span><span class="o">.</span><span class="n">mean</span><span class="p">(</span><span class="n">x</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

  </div>

  

  <div class="
      cell border-box-sizing code_cell rendered">
    <div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># x is log10 P and y is M_V:</span>
<span class="n">x</span><span class="p">,</span> <span class="n">y</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">log10</span><span class="p">(</span><span class="n">ext</span><span class="o">.</span><span class="n">P_d</span><span class="p">),</span> <span class="n">ext</span><span class="o">.</span><span class="n">M_V</span>

<span class="c1"># Apply the linear regression functions defined above:</span>
<span class="n">b</span> <span class="o">=</span> <span class="n">linreg_b</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">y</span><span class="p">)</span>
<span class="n">a</span> <span class="o">=</span> <span class="n">linreg_a</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">y</span><span class="p">,</span> <span class="n">b</span><span class="p">)</span>

<span class="c1"># Print the solution:</span>
<span class="n">md</span><span class="p">(</span><span class="sa">f</span><span class="s2">&quot;The period-luminosity relation reads $M_V = </span><span class="si">{</span><span class="n">a</span><span class="si">:</span><span class="s2">.3f</span><span class="si">}</span><span class="s2"> </span><span class="si">{</span><span class="n">b</span><span class="si">:</span><span class="s2">.3f</span><span class="si">}</span><span class="s2"> \cdot \log P$.&quot;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    


<div class="output_markdown rendered_html output_subarea output_execute_result">
<p>The period-luminosity relation reads $M_V = -1.487 -2.455 \cdot \log P$.</p>

</div>

</div>

</div>
</div>

  </div>
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>A period of 32 days was found for a Cepheid in the galaxy NGC 4321. Its apparent magnitude is $m_V = 25.511$.</p>
<h2 id="What-is-the-distance-to-NGC-4321?">What is the distance to NGC 4321?<a class="anchor-link" href="#What-is-the-distance-to-NGC-4321?">&#182;</a></h2><p>Use the period-luminosity relation you found in (a).</p>
<p>You will nead the distance modulus equation again:</p>
<p>$D = 10^{0.2\,(m_V - M_V +5)}$</p>
<p>Let's translate this to Python code:</p>

</div>
</div>
</div>

  

  <div class="
      cell border-box-sizing code_cell rendered">
    <div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Calculate M_V using a and b as derived above:</span>
<span class="n">M_V</span> <span class="o">=</span> <span class="n">a</span> <span class="o">+</span> <span class="n">b</span> <span class="o">*</span> <span class="n">np</span><span class="o">.</span><span class="n">log10</span><span class="p">(</span><span class="mf">32.</span><span class="p">)</span>

<span class="c1"># Apply the distance modulus:</span>
<span class="n">D</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">power</span><span class="p">(</span><span class="mi">10</span><span class="p">,</span> <span class="mf">0.2</span> <span class="o">*</span> <span class="p">(</span><span class="mf">25.511</span> <span class="o">-</span> <span class="n">M_V</span> <span class="o">+</span> <span class="mi">5</span><span class="p">))</span>

<span class="nb">print</span><span class="p">(</span><span class="sa">f</span><span class="s2">&quot;</span><span class="si">{</span><span class="p">(</span><span class="n">D</span> <span class="o">*</span> <span class="n">u</span><span class="o">.</span><span class="n">pc</span><span class="p">)</span><span class="o">.</span><span class="n">to</span><span class="p">(</span><span class="n">u</span><span class="o">.</span><span class="n">kpc</span><span class="p">)</span><span class="si">:</span><span class="s2">.0f</span><span class="si">}</span><span class="s2">&quot;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    

<div class="output_subarea output_stream output_stdout output_text">
<pre>13753 kpc
</pre>
</div>
</div>

</div>
</div>

  </div>
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Compare-this-with-the-value-found-in-literature.">Compare this with the value found in literature.<a class="anchor-link" href="#Compare-this-with-the-value-found-in-literature.">&#182;</a></h3><p>You can search the <a href="http://ned.ipac.caltech.edu/">NASA/IPAC Extragalactic Database</a> for NGC 4321.</p>
<p>Literature gives a variety of distances ranging from $14 200 - 21 400\,$kpc. Our result is arguably close if you consider that we derived the period-luminosity relation based on only three measurements. A full discussion of the discrepancy would include the uncertainties on all values given in Table 1.</p>

</div>
</div>
</div>



<!-- Loads nbinteract package -->
<script src="https://unpkg.com/nbinteract-core" async></script>
<script>
  (function setupNbinteract() {
    // If NbInteract hasn't loaded, wait one second and try again
    if (window.NbInteract === undefined) {
      setTimeout(setupNbinteract, 1000)
      return
    }

    var interact = new window.NbInteract({
      spec: 'ekaterinailin/cfa041852fe9a35931ac02932c38046e/master',
      baseUrl: 'https://mybinder.org',
      provider: 'gist',
    })
    interact.prepare()

    window.interact = interact
  })()
</script>
    </div>
  </div>
</body>
