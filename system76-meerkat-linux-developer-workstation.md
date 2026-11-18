# Meet the Meerkat: A compact Linux PC with surprising power for developers

How a pint-sized System76 Meerkat became my everyday workstation.

**By Don Watkins**  
**Published:** February 11, 2026  
**Source:** [https://allthingsopen.org/articles/system76-meerkat-linux-developer-workstation](https://allthingsopen.org/articles/system76-meerkat-linux-developer-workstation)

<figure class="featured">
<img src="https://allthingsopen.org/wp-content/uploads/2026/01/tiny-meerkat-rocks-e1769891778484.jpg" class="featured" alt="Tiny Meerkat, with a focused look, perched on a rock." />
<figcaption>Image by <a href="https://pixabay.com/users/storme22k-4337202/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=7913402">Storme Kovacs</a> from <a href="https://pixabay.com//?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=7913402">Pixabay</a></figcaption>
</figure>

A trip to Denver and the System76 factory in 2018 afforded me a chance to meet their technology team and look at the products they were building. One of those was the mini computer they call the <a href="https://system76.com/desktops/meerkat/" target="_blank" rel="noreferrer noopener">Meerkat</a>. I said to the engineer that I spoke to, “That looks like an Intel NUC.” He said, “It is a NUC. We add our branding and software and remarket them.”

## My first experience with a Darter Pro

Soon after my visit to their facility, I purchased a Darter Pro, which I really liked. It had an i7 processor, sixteen gigabytes of RAM, and a 256 GB NVMe drive. It was my first new Linux computer. Prior to that time, I’d always used refurbished units and installed Ubuntu or Fedora.

This was a step up in life. The Darter Pro was a great unit and I used it for writing and wrote a review of my experience with it. I came to understand and appreciate the new computer and the excellent support team that backed up the product. Whenever I had a question about the Darter Pro, there was somebody at System76 who was there to answer my questions.

**Read more: <a href="http://allthingsopen.org/articles/system76-cosmic-desktop" target="_blank" rel="noreferrer noopener">Trying the Cosmic Desktop from System76: A desktop paradigm change</a>**

## **The pivot to desktop: Experimenting with NUCs**

In 2020, when we were all spending much more time on our screens, it never occurred to me to dock the Darter Pro. Remembering my conversation with the System76 engineer, I decided to try an Intel NUC8 connected to a twenty-seven inch display. I liked the system, but around the same time I started exploring gaming on Linux and the decision to equip this unit with a 256 GB NVMe drive began to have serious drawbacks.

I decided to replace it with a new NUC10 barebones kit that I purchased from an internet retailer. The NUC10 had an i7 with 32 gigabytes of RAM and a one terabyte NVMe drive. Now I had plenty of room to explore Linux gaming.

## The DevOne experiment and AI challenges

Then I decided to purchase a new <a href="https://hpdevone.com/" target="_blank" rel="noreferrer noopener">Hewlett-Packard DevOne</a> that came with <a href="http://allthingsopen.org/articles/system76-cosmic-desktop-pop-os-24-04-hands-on" target="_blank" rel="noreferrer noopener">Pop!_OS</a> preinstalled, and I donated the NUC10 to some friends. I purchased a dock and connected the DevOne to the twenty-seven inch display.

That’s when the AI revolution began. I had downloaded Stable Diffusion for Linux and ran into some bottlenecks because the Ryzen 7 that was in the DevOne didn’t have a GPU. I also didn’t like docking and undocking the unit, so I decided to go back to the small footprint NUC connected to the large display.

This time I went with a NUC11 barebones kit that I got from an internet store and equipped with an i7, 64 gigabytes of RAM, and a one terabyte NVMe drive. It was great for everything but AI tasks.

**Read more: <a href="http://allthingsopen.org/articles/system76-cosmic-desktop-pop-os-24-04-hands-on" target="_blank" rel="noreferrer noopener">System76’s COSMIC desktop: A hands-on tour of Pop!_OS 24.04 LTS</a>**

## **Finding the right balance with MacBook Air**

In the interim, I purchased an M2 MacBook Air and replaced it last fall with an M3 MacBook Air, which is great for AI tasks. But I didn’t want to go through the docking experience again. 

I began to research how I could solve the problem, and that led me back to System76 and the Meerkat. After years of experimenting with laptops, NUCs, and MacBooks, I found what I was looking for in the same place I started: System76.

## **Back to the Meerkat: The perfect solution**

The Meerkat had everything I wanted: small footprint and a GPU. Best of all, I knew that if I didn’t like the unit I could send it back. Better than that, I was supporting a business that is based on Linux and open source.

After my unit arrived, I completed a back-up of the system on my NUC11 with Cronopete, I unboxed the Meerkat and installed Linux Mint 22.2 on it along with Cronopete and restored my files.

### **System specifications**

Here’s a snapshot of my system:

``` wp-block-prismatic-blocks
System:
  Host: don-Meerkat Kernel: 6.14.0-29-generic arch: x86_64 bits: 64
  Desktop: Cinnamon v: 6.4.8 Distro: Linux Mint 22.2 Zara
Machine:
  Type: Mini-pc System: System76 product: Meerkat v: meer10
    serial: <superuser required>
  Mobo: ASUSTeK model: NUC15CRBU7 v: 60AS00K0-MBKA23
    serial: <superuser required> UEFI: ASUSTeK v: CRARL579.0023.2025.0319.1038
    date: 03/19/2025
CPU:
  Info: 16-core Intel Core Ultra 7 255H [MCP] speed (MHz): avg: 1005
    min/max: 400/5100:4400:2500
Graphics:
  Device-1: Intel Arrow Lake-P [Intel Graphics] driver: i915 v: kernel
  Device-2: AVerMedia Live Streamer CAM 313 driver: snd-usb-audio,uvcvideo
    type: USB
  Display: x11 server: X.Org v: 21.1.11 with: Xwayland v: 23.2.6 driver: X:
    loaded: modesetting unloaded: fbdev,vesa dri: iris gpu: i915
    resolution: 1920x1080~60Hz
  API: OpenGL v: 4.6 compat-v: 4.5 vendor: intel mesa
    v: 25.0.7-0ubuntu0.24.04.2 renderer: Mesa Intel Graphics (ARL)
Network:
  Device-1: Intel driver: iwlwifi
  Device-2: Intel Ethernet I226-V driver: igc
Drives:
  Local Storage: total: 953.87 GiB used: 158.55 GiB (16.6%)
Info:
  Memory: total: 32 GiB note: est. available: 30.67 GiB used: 3.52 GiB (11.5%)
  Processes: 375 Uptime: 1h 12m Shell: Bash inxi: 3.3.34
```

## More from We Love Open Source

- <a href="http://allthingsopen.org/articles/system76-cosmic-desktop-pop-os-24-04-hands-on" target="_blank" rel="noreferrer noopener">System76’s COSMIC desktop: A hands-on tour of Pop!_OS 24.04 LTS</a>
- <a href="http://allthingsopen.org/articles/popos-24-04-review-cosmic-desktop-two-year-wait" target="_blank" rel="noreferrer noopener">Pop!_OS 24.04 review: Was the two-year w</a>[ait for COSMIC Desktop worth it?](http://allthingsopen.org/articles/popos-24-04-review-cosmic-desktop-two-year-wait)
- <a href="http://allthingsopen.org/articles/system76-cosmic-desktop" target="_blank" rel="noreferrer noopener">Trying the Cosmic Desktop from System76: A desktop paradigm change</a>
- <a href="http://allthingsopen.org/articles/6-best-linux-open-source-tutorials-2025" target="_blank" rel="noreferrer noopener">6 must-read Linux and open source tutorials of the year</a>
- <a href="http://allthingsopen.org/articles/linux-mint-old-windows-upgrade" target="_blank" rel="noreferrer noopener">How Linux Mint saved an eight-year-old PC</a>

This article is adapted from *“<a href="https://donwatkins.info/2025/09/10/tiny-footprint-big-impact-rediscovering-the-meerkat/" target="_blank" rel="noreferrer noopener">Tiny Footprint, Big Impact: Rediscovering the Meerkat</a>“* by Don Watkins, and is republished with permission from the author.

</div>

---

<div class="cc-license">

<a href="https://creativecommons.org/licenses/by-sa/4.0/" rel="license"><img src="https://allthingsopen.org/wp-content/themes/ato-main-2024/img/cc/by-sa.png" title="This work is licensed under a Creative Commons Attribution-Share Alike 4.0 International License." alt="Creative Commons License" /></a>

This work is licensed under a Creative Commons Attribution-Share Alike 4.0 International License.

