---
title: "Coding"
permalink: /coding/
header:
  image: /assets/photography/2009.08.25-Java-Mount-Bromo_wide.jpg
  caption: Mount Bromo, Indonesia, 2009. <i class="fas fa-camera"></i> A. Lépissier
gallery:
  - url: /assets/images/bezier-demo.png
    image_path: /assets/images/bezier-demo.png
    alt: "Demo"
    title: "Demo"
  - url: /assets/images/bezier-1overX.png
    image_path: /assets/images/bezier-1overX.png
    alt: "1 over X"
    title: "1 over X"
  - url: /assets/images/bezier-logX.png
    image_path: /assets/images/bezier-logX.png
    alt: "Log X"
    title: "Log X"
  - url: /assets/images/bezier-cosX.png
    image_path: /assets/images/bezier-cosX.png
    alt: "Cos X"
    title: "Cos X"
  - url: /assets/images/bezier-Xcube.png
    image_path: /assets/images/bezier-Xcube.png
    alt: "X cube"
    title: "X cube"
  - url: /assets/images/bezier-circle.png
    image_path: /assets/images/bezier-circle.png
    alt: "Cartesian circle"
    title: "Cartesian circle"
  - url: /assets/images/bezier-expX.png
    image_path: /assets/images/bezier-expX.png
    alt: "Exp X"
    title: "Exp X"
toc: true
---

I am committed to open science principles and research reproducibility. I am passionate about science communication, and I believe that scientific knowledge should be publicly accessible. Here are some of the projects I have worked on over the years (on the more fun/random side of things). You can find the code repositories for my academic papers on my [GitHub](https://github.com/walice) page.

## Interpolation using Bézier splines

<i class="fab fa-github"></i> [GitHub repository](https://github.com/walice/beziersplines)

Have you ever wondered what smoothing algorithm Excel uses to fit smooth curves on a XY scatter? Have you ever found yourself trying to read Y values off an Excel XY scatter plot? I did.

Microsoft is not transparent about how it creates the smooth fit between data points in the scatter plots. In fact, it uses a type of parametric curve called a Bézier curve; specifically, a third order Bézier curve with 4 control points. It is a type of cubic spline and avoids some of the [oscillation problems](http://en.wikipedia.org/wiki/Runge's_phenomenon) which typically occur when using high degree polynomials for interpolation.

I created an Excel add-in to interpolate along Excel's smooth line scatter plots. The add-in also comes in with a function to linearly interpolate and extrapolate.

The gallery below showcases the performance of the Bézier spline interpolator on a variety of test functions.

{% include gallery 
  caption = "Performance of the interpolation function." %}

## Genetic algorithm

<i class="fab fa-github"></i> [GitHub repository](https://github.com/walice/Genetic-Algorithm)

Inspired by Darwinian natural selection, genetic algorithms (GA) are exercises in combinatorial optimization that can be used to solve hard optimization problems. Genetic algorithms mimic the process of evolution where only the "fittest" individuals survive over many generations. Starting from a randomly generated population, a GA applies a variety of "genetic operators" so that individuals in the population reproduce, mutate, and clone themselves in order to optimize an objective function called the "fitness function".

I created a genetic algorithm to optimize real-valued functions and I applied it to: (1) optimizing non-convex functions and (2) image reconstruction. The algorithm is publicly available and offers 7 different genetic operators for selection, mutation, and crossover.

The algorithm performs well on non-convex functions that are typically hard to optimize: the asymmetric double claw, the Rosenbrock function, and the Rastrigin function.

The images below show how the genetic algorithm performs for image reconstruction. Starting from randomly generated pixels, the algorithm converges after several iterations and is able to recreate the original image.

![Abraham Lincoln](/assets/images/genetic-lincoln.png)

![Albert Einstein](/assets/images/genetic-einstein.png)

## SkyShares

**Check out the website at [www.skyshares.org](http://www.skyshares.org/).**

<i class="fab fa-github"></i> [GitHub repository](https://github.com/walice/skyshares)

While I was at the [Center for Global Development](https://www.cgdev.org/), I created an interactive tool that allows users to simulate the economic and environmental implications of a climate deal called [SkyShares](http://www.skyshares.org/). You can find more information on SkyShares in the [climate change section](/research/02-climatechange//#skyshares) of my research page.

SkyShares is publicy available and open source. It is written in JavaScript with a Node.js back-end and a MongoDB database. SkyShares also exists as a stand-alone Excel interactive workbook (see the documentation tab of SkyShares to download SkyShares Desktop).

The website allows users to select which countries will participate in the climate coalition, and to choose parameters of the climate deal such as the temperature target and how much trading to allow. The website then calculates the carbon budget, financial flows, and decarbonization costs that would ensue as a result. Users can visualize the evolution of the financial flows between countries in the future.

The simulation below displays what the financial flows would be (buyers of carbon are in red, sellers of carbon are in black) as a result of a carbon budget consistent with a 2°C target, an allocation rule converging to per capita shares in 2030, and full carbon trading.

![SkyShares evolution of financial flows](/assets/images/skyshares-evolution-flows.gif)