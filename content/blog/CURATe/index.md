---
title: Benchmarking Personalised LLM Agent Alignment
summary: Developed benchmark and pipeline to evaluate large language models' ability to attend to and appropriately handle user-specific safety-critical context in recommendations. 
date: 2024-10-28

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
# image:
#   caption: 'Image credit: [**Unsplash**](https://unsplash.com)'

# authors:
#   - admin
#   - Ted

# tags:
#   - Academic
#   - Hugo Blox
#   - Markdown

# content_meta:
#   trending: true
---

Developed benchmark and pipeline to evaluate large language models' ability to attend to and appropriately handle user-specific safety-critical context in recommendations. This project was completed as a part of my DPhil at the University of Oxford, in collaboration with <a href = 'https://foersterlab.com/' target = '_blank'>Foerster Lab for AI Research (FLAIR)</a> in Oxford's Department of Engineering Science.

## Timeline

Aug 2024 - Nov 2024

## Collaborators
<ul>
  <!-- <li><b>Lize Alberts</b>, Human-Centred AI, Dept. Computer Science, University of Oxford</li> -->
  <li><a href = 'https://research.vu.nl/en/persons/marcos-oliveira' target = '_blank'>Benjamin Ellis</a>, FLAIR, Dept. Engineering Science, University of Oxford</li>
  <li><a href = 'https://research.vu.nl/en/persons/marcos-oliveira' target = '_blank'>Andrei Lupu</a>, FLAIR, Dept. Engineering Science, University of Oxford</li>
  <li><a href = 'https://research.vu.nl/en/persons/marcos-oliveira' target = '_blank'>Prof. Jakob Foerster</a>, FLAIR, Dept. Engineering Science, University of Oxford</li>
</ul>


## Project Summary

<!-- give context, why, how it relates to other work, future work, reference paper, talk about how it relates to current work -->

We introduce a multi-turn benchmark for evaluating personalised alignment in LLM-based AI assistants, focusing on their ability to handle user-provided safety-critical contexts. Our assessment of ten leading models across five scenarios (with 337 use cases each) reveals systematic inconsistencies in maintaining user-specific consideration, with even top-rated "harmless" models making recommendations that should be recognised as obviously harmful to the user given the context provided. Key failure modes include inappropriate weighing of conflicting preferences, sycophancy (prioritising desires above safety), a lack of attentiveness to critical user information within the context window, and inconsistent application of user-specific knowledge. The same systematic biases were observed in OpenAI's o1, suggesting that strong reasoning capacities do not necessarily transfer to this kind of personalised thinking. We find that prompting LLMs to consider safety-critical context significantly improves performance, unlike a generic 'harmless and helpful' instruction. Based on these findings, we propose research directions for embedding self-reflection capabilities, online user modelling, and dynamic risk assessment in AI assistants. Our work emphasises the need for nuanced, context-aware approaches to alignment in systems designed for persistent human interaction, aiding the development of safe and considerate AI assistants.

<!-- Welcome 👋

{{< toc mobile_only=true is_open=true >}}

## Overview

1. The Hugo Blox website builder for Hugo, along with its starter templates, is designed for professional creators, educators, and teams/organizations - although it can be used to create any kind of site
2. The template can be modified and customised to suit your needs. It's a good platform for anyone looking to take control of their data and online identity whilst having the convenience to start off with a **no-code solution (write in Markdown and customize with YAML parameters)** and having **flexibility to later add even deeper personalization with HTML and CSS**
3. You can work with all your favourite tools and apps with hundreds of plugins and integrations to speed up your workflows, interact with your readers, and much more

[//]: # '[![The template is mobile first with a responsive design to ensure that your site looks stunning on every device.](https://raw.githubusercontent.com/HugoBlox/hugo-blox-builder/main/starters/academic-cv/preview.png)](https://hugoblox.com)'

### Get Started

> [!TIP]+ Quick Start Guide
> New to Hugo Blox? Follow these steps to get your site up and running in minutes!

- 👉 [**Create a new site**](https://hugoblox.com/templates/)
- 📚 [**Personalize your site**](https://docs.hugoblox.com/)
- 💬 [Chat with the **Hugo Blox community**](https://discord.gg/z8wNYzb) or [**Hugo community**](https://discourse.gohugo.io)
- 🐦 Twitter: [@GetResearchDev](https://x.com/BuildLore) [@GeorgeCushen](https://twitter.com/GeorgeCushen) #MadeWithHugoBlox
- 💡 [Request a **feature** or report a **bug** for _Hugo Blox_](https://github.com/HugoBlox/hugo-blox-builder/issues)
- ⬆️ **Updating Hugo Blox?** View the [Update Guide](https://docs.hugoblox.com/reference/update/) and [Release Notes](https://github.com/HugoBlox/hugo-blox-builder/releases)

> [!IMPORTANT]
> Remember to backup your site before making major updates!

## Crowd-funded open-source software

To help us develop this template and software sustainably under the MIT license, we ask all individuals and businesses that use it to help support its ongoing maintenance and development via sponsorship.

### [❤️ Click here to become a sponsor and help support Hugo Blox's future ❤️](https://hugoblox.com/sponsor/)

As a token of appreciation for sponsoring, you can **unlock [these](https://hugoblox.com/sponsor/) awesome rewards and extra features 🦄✨**

## Ecosystem

- **[Bibtex To Markdown](https://github.com/GetRD/academic-file-converter):** Automatically import publications from BibTeX

## Inspiration

[Learn what other **creators**](https://hugoblox.com/creators/) are building with this template.

## Features

> [!NOTE]+ Enhanced Markdown Support  
> Hugo Blox now supports GitHub and Obsidian-style callouts! Use standard Markdown alert syntax like `> [!NOTE]` for better portability.

- **Page builder** - Create _anything_ with no-code [**blocks**](https://hugoblox.com/blocks/) and [**elements**](https://docs.hugoblox.com/reference/markdown/)
- **Edit any type of content** - Blog posts, publications, talks, slides, projects, and more!
- **Create content** in [**Markdown**](https://docs.hugoblox.com/reference/markdown/), [**Jupyter**](https://docs.hugoblox.com/getting-started/cms/), or [**RStudio**](https://docs.hugoblox.com/getting-started/cms/)
- **Plugin System** - Fully customizable [**color** and **font themes**](https://docs.hugoblox.com/getting-started/customize/)
- **Display Code and Math** - Code syntax highlighting and LaTeX math supported
- **Integrations** - [Google Analytics](https://analytics.google.com), [Disqus commenting](https://disqus.com), Maps, Contact Forms, and more!
- **Beautiful Site** - Simple and refreshing one-page design
- **Industry-Leading SEO** - Help get your website found on search engines and social media
- **Media Galleries** - Display your images and videos with captions in a customizable gallery
- **Mobile Friendly** - Look amazing on every screen with a mobile friendly version of your site
- **Multi-language** - 35+ language packs including English, 中文, and Português
- **Multi-user** - Each author gets their own profile page
- **Privacy Pack** - Assists with GDPR
- **Stand Out** - Bring your site to life with animation, parallax backgrounds, and scroll effects
- **One-Click Deployment** - No servers. No databases. Only files.

> [!WARNING]+ Version Requirements  
> The new Markdown alert syntax requires Hugo v0.132.0 or later. Make sure you're using a compatible version!

## Themes

Hugo Blox and its templates come with **automatic day (light) and night (dark) mode** built-in. Visitors can choose their preferred mode by clicking the sun/moon icon in the header.

[Choose a stunning **theme** and **font**](https://docs.hugoblox.com/getting-started/customize/) for your site. Themes are fully customizable.

## License

Copyright 2016-present [George Cushen](https://georgecushen.com).

Released under the [MIT](https://github.com/HugoBlox/hugo-blox-builder/blob/main/LICENSE.md) license. -->
