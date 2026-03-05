---
layout: page
title: Doomsday Globe
description: Real-time visualization of global conflicts and an aggregated Global Threat Level.
url: https://www.doomsdayglobe.com/
img: assets/img/DoomsdayGlobe.png
importance: 3
category: fun
---

This idea came from watching recent world conflicts unfold. I wanted a simple way to visualise what’s happening globally and show an aggregated Global Threat Level in one place and thats how [DoomsdayGlobe](https://www.doomsdayglobe.com/) came into existence.

Using [lovable.ai](https://lovable.dev/), I built a working site in about three hours that displays real-time global conflicts on an interactive globe.

This is only my second website (after [nznux.com](https://nznux.com/)), and I was genuinely surprised at how capable and accessible AI tools have become. It really feels like web building has been democratized — you can go from idea to live product incredibly fast.

Steps
1. Get domain name, I prefer [Cloudflare](https://domains.cloudflare.com/), cost wasa $5-7 p.a
2. Create an account on  [lovable.ai](https://lovable.dev/)
3. Create a detailed markdown doc that I gave the AI tool to think through all of what I wanted it to build
4. For the Globe library I pulled from [globe.gl](https://globe.gl/) 
5. Monitered the AI output - when it begins to hallucinate, I corrected it to bring back on track
6. Ran out of free credits, purchased a one off $20 credit to finish the build
7. Since lovable didn’t offer free hosting at the time, I deployed the site on [vercel ](https://vercel.com/) using a free account.  

Results

The site now receives around 4,000 organic page views per month. That may not be huge, but traffic wasn’t the main goal.

The real achievement for me was proving that an idea could be turned into a working product in just a few hours using AI.


What’s Next

The next update is to make the threat level update fully in real time.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/DoomsdayGlobe.png" title="DoomsdayGlobe" alt="Screenshot of Doomsday Globe showing global conflict locations and threat level" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    <a href="https://www.doomsdayglobe.com/" target="_blank" rel="noopener">DoomsdayGlobe — live site</a>
</div>