---
title: "How to easily make a GenAI SVG logo"
date: 2024-12-17T12:28:05+01:00
draft: false
---

Recently, I needed a logo for a project I am working. I love SVG images for their versatility, but have the ability nor interest in creating on myself from scratch.
So why not use an LLM for this?

I tried to create an SVG directly with all the current (2024-12-17) easily available offerings[^list-of-models].
They all failed miserably.

<figure style="max-width:80%">
<!--	{{ readFile "static/imgs/genai-svg-logo/logo1.svg" | safeHTML }}-->
	<img src="/imgs/genai-svg-logo/logo1.svg" />
<figcaption>
Figure 1: SVG "icon depicting two fingers (one human, one robotic) holding a Sharpie-style pen", according to OpenAI GPT-4o.
</figcaption>
</figure>

This was not working out, so instead I opted to first generate the image "in vector art style" and then convert it to svg using [this](https://online.rapidresizer.com/tracer.php) useful tool which traces the image and converts it to svg flawlessly.

<figure style="max-width:80%">
	<img src="/imgs/genai-svg-logo/sharpie-logo.svg" />
<figcaption>
Figure 2: SVG created by converting a regular rendered icon created by OpenAI GPT-4o in webp format to SVG using Rapid Resizer's tracing tool.
</figcaption>
</figure>

Not bad!


[^list-of-models]: OpenAI GPT-4o, Anthropic Claude-3.5-Haiku, Google Gemini/Imagen-3.

