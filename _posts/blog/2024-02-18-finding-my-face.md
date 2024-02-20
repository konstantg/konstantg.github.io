---
layout: post
comments: true
category: blog
title: Finding my face
description: Experimenting with Midjourney's face generation.
image: "/assets/img/posts/2024-02-18-finding-my-face/1.jpg"
tags: [experiments, generative ai, ai, midjourney, chatgpt]
---

<div class="img_full">
    <img style="width: 100%;" src="{{page.image}}">
    <figcaption></figcaption>
</div>

My brother shared a [TikTok](https://www.tiktok.com/@ai_tools_help/photo/7308047954881809696){:target="_blank"} with me a couple of months ago. It is supposed to depict what DALL·E, OpenAI's text-to-image model, comes up with when asked for an image of "a Swedish guy" and then gradually increasing the "Swedishness" factor more and more. Ignoring the cultural caricature of IKEA logos and meatballs in Valhalla for a moment, the reason my brother sent this to me is because the second to last image, the one labelled "LET ME SEE THE FINAL FORM", the one just before Anthony Hopkins as Odin, is actually an image of *me*.

Or at least it looks like me. It definitely passes the "mom test". This is the very scientific test where I show my mother the picture and she says "That is you!" confirming the similarity.

I have been thinking recently about what would be the best way to navigate the latent space of generative AI models, that is the space of all possible images that they can produce. This post is a quick attempt to experiment with this latent space exploration and to generate my face with Midjourney, similar to what the TikTok creator achieved coincidentally.

Currently, language is the main approach. You put the image you have in mind, your image intention, into words which are then used to guide the image generation. We call this process text-to-image. However this assumes that you know which words to use. The reverse procedure, image-to-text, can help with the vocabulary. [ChatGPT 4](https://chat.openai.com/){:target="_blank"} and [Midjourney](https://www.midjourney.com/home){:target="_blank"} both provide image-to-text tools so let us test them out.

## Describing images

Here is one example. ChatGPT 4 gives the following description when prompted with this photo of Pixel, our Irish terrier, and asked about its content.

<div class="aside-left">
    <img style="width: 100%;" src="/assets/img/posts/2024-02-18-finding-my-face/2.jpg">
    <figcaption>Pixel in Czechia, 2019.</figcaption>
</div>


<span style="font-family: Inconsolata;">The image shows a brown dog sitting on a grassy field with a forested landscape in the background. The dog appears to be of a wire-haired breed, possibly a terrier, with its tongue out, indicating it might be panting or hot. It has a black harness on. The setting looks like a rural area, and there are round hay bales scattered in the distance across the field. The sky is overcast, suggesting it may be a cool or humid day.</span>

Pretty accurate. It even goes beyond just describing the content and makes assumptions about the dog's state and the weather conditions.

Using Midjourney's `/describe` command is a different story. Give it an image and it generates four possible text prompts for that image. Here they are for the same image of Pixel:

1. <span style="font-family: Inconsolata">a small brown dog sitting in an open field, in the style of analogue filmmaking, documentary travel photography, high quality photo, playful use of line, british topographical, strong facial expression, verdadism --ar 51:64</span>
2. <span style="font-family: Inconsolata">a brown dog is sitting on the grass with his tongue, in the style of analogue filmmaking, french countryside, scottish landscapes, documentary travel photography, light amber and green, topographical views, soviet --ar 51:64</span>
3. <span style="font-family: Inconsolata">one plovd dog in a field., in the style of photo taken with fujifilm superia, briton rivière, kurzgesagt, monumental vistas, green and amber, playful use of line, charming, idyllic rural scenes --ar 51:64</span>
4. <span style="font-family: Inconsolata">dog is sitting at the beck in a grassland, in the style of analogue filmmaking, light brown and green, documentary travel photography, cluj school, manticore, made of rubber, playful expressions --ar 51:64</span>

Plovd dog? Kurzgesagt? Made of rubber? You can see that the semantics are a bit off. Midjourney's descriptions should not be taken literally. They are meant to capture the vibe and style, not just the content. The keywords are present but they are shuffled in a way that doesn't always make sense. A *word soup*. 

<div class="aside-right">
    <img style="width: 100%;" src="/assets/img/posts/2024-02-18-finding-my-face/3.jpg">
    <figcaption>Fake Pixel wishing he was a real good boy.</figcaption>
</div>

Nevertheless, these prompts show you how to set up an effective prompt that will get similar looking results. Midjourney teaches me that "british topographical" and "verdadism" are appropriate descriptions for the photo, prompts that I wouldn't otherwise have thought of using. So let's try them out.

Using the first description as a prompt we generate this image. Not bad. We can use this as a starting point to make the obvious corrections. For example, "small brown dog" should be "an Irish terrier". A few minutes later, with some prompt engineering, we should be able to generate an image closer to the original one. But let's do something more interesting.

<br>

## Describe me

What about faces? How well does Midjourney describe a face? I am willing to volunteer for this experiment.

<div class="aside-left">
    <img style="width: 100%;" src="/assets/img/posts/2024-02-18-finding-my-face/4.jpg">
    <figcaption>My 2023 LinkedIn face.</figcaption>
</div>

Let's use the photograph that is currently on my [SINTEF webpage](https://www.sintef.no/en/all-employees/employee/konstantinos.gavriil/){:target="_blank"}. The very first description I get from Midjourney is:

<span style="font-family: Inconsolata;">jd 'jab mrm's picture, senior developer, in the style of soviet lens, studio portrait, pixelation, grey academia, poetcore, rtx on, hyperrealistic portraiture --ar 127:128</span>

Poetcore senior developer. Sure. Why not? As expected, we get a word soup of various styles. Using them as prompts gets us close to the image. Unsurprisingly, we never get the same exact face. You can only do so much with words. Which leads us to the next test.

Midjourney's `/imagine` command can also accept an image as input. This influences the result but does not guarantee similarity. Using my photo as a prompt, weighted with the maximum factor of 3, followed by a `white shirt` request we get:

<div class="img_full">
    <img style="width: 100%;" src="/assets/img/posts/2024-02-18-finding-my-face/5.png">
    <figcaption>Let me introduce you to my extended family.</figcaption>
</div>

Still not my face. More like distant relative likeness. Midjourney uses input images as influence, so there is no hard constraint in place to preserve any part of the image's content. However, we get to see how Midjourney "views" my face. Where in its latent space of representations it holds my likeness. Which are the closest images to my photo it can generate.

This is very much affected by the training data and the generalization capability of the AI model. If it has never "seen" my face then it has to interpolate or extrapolate it from its training data. Similar to what the generative adversarial network (GAN) of [thispersondoesnotexist.com](https://thispersondoesnotexist.com/){:target="_blank"} does.

Unlike GANs though that have been trained to generate images, diffusion models such as Midjourney do something different. They have been trained on removing noise from images. The generation process happens by repeatedly adding and removing noise to an image until we get a clear result. I will not go into detail and instead mention that [the geometry of this latent space is more interesting](https://arxiv.org/abs/2307.12868){:target="_blank"}.

## Final quiz

I will leave you with a quiz. Comment below if you know which famous painting ChatGPT is describing here.

> It features a surreal landscape with a barren, desert-like setting under a vast, calm sky transitioning from yellow to blue, indicative of twilight. Central to the scene are several melting watches draped over objects, suggesting the fluidity and unreliability of time. One watch hangs limply from the branch of a barren tree. Another drapes over the edge of a rectangular object that could be interpreted as a table or block. The third watch, its face visible, slumps over a strange, amorphous, flesh-like form in the center, which is reminiscent of a sleeping face with a long eyelash. This form rests on the flat surface, which abruptly meets the sea at the horizon. The fourth watch, closed and swarming with ants, lies on the left side, on the flat surface. The backdrop features a cliff face over the sea, under the wide expanse of the sky. The painting is renowned for its dream-like, fantastical imagery and thought-provoking representation of time.