+++
date  = 2022-11-01
+++

{{ resize_image(path="/CPURaytracerThumbnail.png", width=160, height=320, op="fit_height") }}<br clear="all" />
{{ set_headline(text="CPU Raytracer") }}
A short summary of a C/C++ raytracer project capable of rendering <br/>a mildly complex scene in close to real-time.<br/>
<em>(3D mesh made by <a href="https://www.cgtrader.com/ozne000"><u>Ozne000</u></a>)</em>

<!-- more -->

## Why?
I wanted to learn some fundamental principles of graphics rendering without having to deal
with the overhead of learning a graphics API at the same time. 

Furthermore, I was interested in seeing how fast I can make this renderer run, without
ratholing too much on any specific part while also minimizing dependencies.

## Some achievements
I became more comfortable dealing with things like coordinate transformations, parsing and processing OBJ files,
Compiling and running without the CRT, generating acceleration structures for ray-tracing and multi-threading.  

## Things to improve
Aside from the countless things that could be added, profiling and debug visualisation seem like the most important ones.

I was able to get away with no debug visualisation and only basic frame timing, due to the small scale
and hard-coded nature of the project.
But generally, these things are a must to gather real information about the run-time
behaviour of a program, so that one can improve things in a reality-based manner.

## Further experiments
There are some rendering features I would like to explore if I had infinite time and money.

- **Soft shadows.** Instead of using a bruteforced sampling approach, experiment with other techniques
like ray-marching.

- **Beyond Blinn-Phong.** Try using BSDFs instead.

- **...**
<br/>
## Some more renders
<br/>
{{ resize_image(path="/CPURaytracerPic0.png", width=160, height=320, op="fit_height") }}
<br/>
{{ resize_image(path="/CPURaytracerPic1.png", width=160, height=320, op="fit_height") }}
<br clear="all" />