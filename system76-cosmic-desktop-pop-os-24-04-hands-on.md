# System76’s COSMIC desktop: A hands-on tour of Pop!_OS 24.04 LTS

How System76's new desktop environment prioritizes accessibility, customization, and user choice.

**By Don Watkins**  
**Published:** January 21, 2026  
**Source:** [https://allthingsopen.org/articles/system76-cosmic-desktop-pop-os-24-04-hands-on](https://allthingsopen.org/articles/system76-cosmic-desktop-pop-os-24-04-hands-on)

System76 is celebrating 20 years, and they’re marking the occasion with the official <a href="https://system76.com/pop/" target="_blank" rel="noreferrer noopener">release of Pop!_OS 24.04 LTS</a> and the COSMIC desktop environment. As Carl Richell, System76’s CEO, explained in the announcement: “*COSMIC is built on the ethos that the best open source projects enable people to not only use them, but to build with them. COSMIC is modular and composable. It’s the flagship experience for Pop!\_OS in its own way, and can be adapted by anyone who wants to build their own unique user experience for Linux.*“

## The journey to COSMIC

I’ve been following the development of COSMIC for the past four years. System76 had been customizing GNOME for Pop!\_OS, which first launched on October 27, 2017, with Ubuntu 17.10. The operating system was designed to provide a clean, productivity-focused experience, featuring full-disk encryption by default, curated drivers for NVIDIA GPUs, and a streamlined installer. Over time, System76 introduced its own desktop environment tweaks, which ultimately led to the development of the COSMIC desktop. This project began in 2021 and has become fully independent—a complete reimagining of what a Linux desktop environment can be.

When the release announcement hit my inbox in December, I was excited to <a href="https://system76.com/pop/download/" target="_blank" rel="noreferrer noopener">download</a> it and try it out on a spare laptop with an i7 processor and 16 GB of RAM. I downloaded the ISO file, created a bootable drive, and started the installation process.

**Read more: <a href="http://allthingsopen.org/articles/popos-24-04-review-cosmic-desktop-two-year-wait" target="_blank" rel="noreferrer noopener">Pop!_OS 24.04 review: Was the two-year w</a>[ait for COSMIC Desktop worth it?](http://allthingsopen.org/articles/popos-24-04-review-cosmic-desktop-two-year-wait)**

## Getting started: Installation

As usual with Pop!\_OS, the installation was extremely easy and well-designed. The installation proceeded just like <a href="http://allthingsopen.org/articles/system76-cosmic-desktop" target="_blank" rel="noreferrer noopener">previous Pop!_OS installations</a>, with the familiar, streamlined interface guiding me through each step.

<div class="wp-block-image">

<figure class="aligncenter size-full">
<img src="http://allthingsopen.org/wp-content/uploads/2026/01/COSMIC-desktop_first-screen.png" class="wp-image-8338" data-fetchpriority="high" decoding="async" srcset="https://allthingsopen.org/wp-content/uploads/2026/01/COSMIC-desktop_first-screen.png 1024w, https://allthingsopen.org/wp-content/uploads/2026/01/COSMIC-desktop_first-screen-300x206.png 300w, https://allthingsopen.org/wp-content/uploads/2026/01/COSMIC-desktop_first-screen-768x527.png 768w" sizes="(max-width: 1024px) 100vw, 1024px" width="1024" height="703" alt="Pop!_OS 24.04 LTS COSMIC desktop installation: First screen" />
<figcaption>Screen capture by Don Watkins, CC-BY-SA 4.0</figcaption>
</figure>

</div>

I decided to do a clean install, erasing the recently installed Fedora KDE Plasma.

<div class="wp-block-image">

<figure class="aligncenter size-full">
<img src="http://allthingsopen.org/wp-content/uploads/2026/01/COSMIC-desktop_clean-install.png" class="wp-image-8337" decoding="async" srcset="https://allthingsopen.org/wp-content/uploads/2026/01/COSMIC-desktop_clean-install.png 1024w, https://allthingsopen.org/wp-content/uploads/2026/01/COSMIC-desktop_clean-install-300x194.png 300w, https://allthingsopen.org/wp-content/uploads/2026/01/COSMIC-desktop_clean-install-768x497.png 768w" sizes="(max-width: 1024px) 100vw, 1024px" width="1024" height="662" alt="Pop!_OS 24.04 LTS COSMIC desktop installation: Choose installation type - clean" />
<figcaption>Screen capture by Don Watkins, CC-BY-SA 4.0</figcaption>
</figure>

</div>

I was invited to create a user and provide a password.

<div class="wp-block-image">

<figure class="aligncenter size-full">
<img src="http://allthingsopen.org/wp-content/uploads/2026/01/COSMIC-desktop_user-creation.png" class="wp-image-8336" decoding="async" srcset="https://allthingsopen.org/wp-content/uploads/2026/01/COSMIC-desktop_user-creation.png 768w, https://allthingsopen.org/wp-content/uploads/2026/01/COSMIC-desktop_user-creation-300x219.png 300w" sizes="(max-width: 768px) 100vw, 768px" width="768" height="561" alt="Pop!_OS 24.04 LTS COSMIC desktop installation: Create a username and password" />
<figcaption>Screen capture by Don Watkins, CC-BY-SA 4.0</figcaption>
</figure>

</div>

I chose not to encrypt my disk, but it’s all set up to use your user password as the encryption password unless otherwise specified.

<div class="wp-block-image">

<figure class="aligncenter size-full">
<img src="http://allthingsopen.org/wp-content/uploads/2026/01/COSMIC-desktop_encryption.png" class="wp-image-8335" decoding="async" srcset="https://allthingsopen.org/wp-content/uploads/2026/01/COSMIC-desktop_encryption.png 768w, https://allthingsopen.org/wp-content/uploads/2026/01/COSMIC-desktop_encryption-300x219.png 300w" sizes="(max-width: 768px) 100vw, 768px" width="768" height="561" alt="Pop!_OS 24.04 LTS COSMIC desktop installation: Choose encryption type" />
<figcaption>Screen capture by Don Watkins, CC-BY-SA 4.0</figcaption>
</figure>

</div>

Installation proceeded quickly on my laptop. When the initial install was finished, I was invited to restart the computer. That’s when I began to see the changes brought by the COSMIC desktop.

<div class="wp-block-image">

<figure class="aligncenter size-full">
<img src="http://allthingsopen.org/wp-content/uploads/2026/01/COSMIC-desktop_login.png" class="wp-image-8334" decoding="async" srcset="https://allthingsopen.org/wp-content/uploads/2026/01/COSMIC-desktop_login.png 768w, https://allthingsopen.org/wp-content/uploads/2026/01/COSMIC-desktop_login-300x126.png 300w" sizes="(max-width: 768px) 100vw, 768px" width="768" height="323" alt="Pop!_OS 24.04 LTS COSMIC desktop installation: Login after reboot" />
<figcaption>Screen capture by Don Watkins, CC-BY-SA 4.0</figcaption>
</figure>

</div>

## First login: Accessibility takes center stage

Wow, this was a new feature! At the bottom-left of the initial login screen, I noticed I could set my accessibility options, including a screen reader, magnifier, high contrast, and inverted colors. This is such an important option for those of us who need accessibility options from the first login.

<div class="wp-block-image">

<figure class="aligncenter size-full">
<img src="http://allthingsopen.org/wp-content/uploads/2026/01/COSMIC-desktop_welcome.png" class="wp-image-8333" decoding="async" srcset="https://allthingsopen.org/wp-content/uploads/2026/01/COSMIC-desktop_welcome.png 768w, https://allthingsopen.org/wp-content/uploads/2026/01/COSMIC-desktop_welcome-300x162.png 300w" sizes="(max-width: 768px) 100vw, 768px" width="768" height="415" alt="Pop!_OS 24.04 LTS COSMIC desktop installation: Welcome screen" />
<figcaption>Screen capture by Don Watkins, CC-BY-SA 4.0</figcaption>
</figure>

</div>

On the next screen, I can set the screen reader, interface size, additional scale options, and the magnifier. Kudos to System76 for putting accessibility first in COSMIC. The next screen is my chance to connect to the wireless networks I will be using. Following that is the choice of language I will be using. Then a screen to set the keyboard layout, time zone, and location.

<div class="wp-block-image">

<figure class="aligncenter size-full">
<img src="http://allthingsopen.org/wp-content/uploads/2026/01/COSMIC-desktop_date-time.png" class="wp-image-8332" decoding="async" srcset="https://allthingsopen.org/wp-content/uploads/2026/01/COSMIC-desktop_date-time.png 768w, https://allthingsopen.org/wp-content/uploads/2026/01/COSMIC-desktop_date-time-300x162.png 300w" sizes="(max-width: 768px) 100vw, 768px" width="768" height="414" alt="Pop!_OS 24.04 LTS COSMIC desktop installation: Set date, time, and location" />
<figcaption>Screen capture by Don Watkins, CC-BY-SA 4.0</figcaption>
</figure>

</div>

## Customizing your desktop experience

This is where COSMIC really shines—the level of customization available right from the first setup is impressive.

Next, I am provided with options for how I want my desktop to look. This is too cool!

<div class="wp-block-image">

<figure class="aligncenter size-full">
<img src="http://allthingsopen.org/wp-content/uploads/2026/01/COSMIC-desktop_appearance.png" class="wp-image-8331" decoding="async" srcset="https://allthingsopen.org/wp-content/uploads/2026/01/COSMIC-desktop_appearance.png 768w, https://allthingsopen.org/wp-content/uploads/2026/01/COSMIC-desktop_appearance-300x164.png 300w" sizes="(max-width: 768px) 100vw, 768px" width="768" height="419" alt="Pop!_OS 24.04 LTS COSMIC desktop installation: Set personal appearance, dark or light mode" />
<figcaption>Screen capture by Don Watkins, CC-BY-SA 4.0</figcaption>
</figure>

</div>

Next, I can choose how I want the dock to appear on my desktop. They really considered all the options I might want to <a href="https://system76.com/pop/customization/" target="_blank" rel="noreferrer noopener">customize my workspace</a>, giving me maximum flexibility to tailor my workflow.

<div class="wp-block-image">

<figure class="aligncenter size-full">
<img src="http://allthingsopen.org/wp-content/uploads/2026/01/COSMIC-desktop_layout.png" class="wp-image-8330" decoding="async" srcset="https://allthingsopen.org/wp-content/uploads/2026/01/COSMIC-desktop_layout.png 768w, https://allthingsopen.org/wp-content/uploads/2026/01/COSMIC-desktop_layout-300x164.png 300w" sizes="(max-width: 768px) 100vw, 768px" width="768" height="421" alt="Pop!_OS 24.04 LTS COSMIC desktop installation: Layout configuration options" />
<figcaption>Screen capture by Don Watkins, CC-BY-SA 4.0</figcaption>
</figure>

</div>

## Window management: Float or tile

Choose whether your windows will float or tile—a choice that fundamentally changes how you work with multiple applications.

<div class="wp-block-image">

<figure class="aligncenter size-full">
<img src="http://allthingsopen.org/wp-content/uploads/2026/01/COSMIC-desktop_workspaces.png" class="wp-image-8329" decoding="async" srcset="https://allthingsopen.org/wp-content/uploads/2026/01/COSMIC-desktop_workspaces.png 768w, https://allthingsopen.org/wp-content/uploads/2026/01/COSMIC-desktop_workspaces-300x163.png 300w" sizes="(max-width: 768px) 100vw, 768px" width="768" height="418" alt="Pop!_OS 24.04 LTS COSMIC desktop installation: Workspace options" />
<figcaption>Screen capture by Don Watkins, CC-BY-SA 4.0</figcaption>
</figure>

</div>

Then, an introduction to <a href="https://support.system76.com/articles/pop-cosmic-keyboard-shortcuts/" target="_blank" rel="noreferrer noopener">keyboard shortcuts</a> to make window management easier.

<div class="wp-block-image">

<figure class="aligncenter size-full">
<img src="http://allthingsopen.org/wp-content/uploads/2026/01/COSMIC-desktop_shortcuts.png" class="wp-image-8328" decoding="async" srcset="https://allthingsopen.org/wp-content/uploads/2026/01/COSMIC-desktop_shortcuts.png 768w, https://allthingsopen.org/wp-content/uploads/2026/01/COSMIC-desktop_shortcuts-300x165.png 300w" sizes="(max-width: 768px) 100vw, 768px" width="768" height="423" alt="Pop!_OS 24.04 LTS COSMIC desktop installation: Keyboard shortcuts" />
<figcaption>Screen capture by Don Watkins, CC-BY-SA 4.0</figcaption>
</figure>

</div>

## Why COSMIC matters

The COSMIC desktop represents a significant shift in the way we interact with Linux environments. It’s not only visually appealing but also highly functional, streamlining workflows and enhancing user experience. What struck me most during this installation was how thoughtfully System76 has considered every user’s needs—from accessibility options available at the very first screen to granular customization of workspace behavior.

The desktop environment’s modular and composable architecture means it’s built to be adapted and extended, embodying the best principles of open source development. For those interested in exploring COSMIC’s development and technical features further, the detailed articles on the <a href="https://blog.system76.com/post/pop-os-letter-from-our-founder" target="_blank" rel="noreferrer noopener">System76 blog</a> provide excellent deep dives into what makes this desktop environment tick.

I find myself increasingly tempted to make COSMIC the primary interface for my System76 Meerkat, as its sleek design and innovative features are making a strong case for a permanent switch. After 20 years of building open source hardware and software, System76 has delivered something special with COSMIC—a desktop environment that respects users’ choices while making Linux more accessible and productive than ever.

## More from We Love Open Source

- <a href="http://allthingsopen.org/articles/popos-24-04-review-cosmic-desktop-two-year-wait" target="_blank" rel="noreferrer noopener">Pop!_OS 24.04 review: Was the two-year w</a>[ait for COSMIC Desktop worth it?](http://allthingsopen.org/articles/popos-24-04-review-cosmic-desktop-two-year-wait)
- <a href="http://allthingsopen.org/articles/system76-cosmic-desktop" target="_blank" rel="noreferrer noopener">Trying the Cosmic Desktop from System76: A desktop paradigm change</a>
- <a href="http://allthingsopen.org/articles/6-best-linux-open-source-tutorials-2025" target="_blank" rel="noreferrer noopener">6 must-read Linux and open source tutorials of the year</a>
- <a href="http://allthingsopen.org/articles/10-free-open-source-tools-work-privacy-creativity" target="_blank" rel="noreferrer noopener">Everyday empowerment: 10 open source tools for life</a>
- <a href="http://allthingsopen.org/articles/linux-mint-old-windows-upgrade" target="_blank" rel="noreferrer noopener">How Linux Mint saved an eight-year-old PC</a>

This article is adapted from “*<a href="https://donwatkins.info/2025/12/11/system76-celebrates-20-years-with-pop_os-and-the-new-cosmic-desktop/" target="_blank" rel="noreferrer noopener">System76 Celebrates 20 Years with Pop!_OS and the New COSMIC Desktop</a>*” by Don Watkins, and is republished with permission from the author.

</div>

---

<div class="cc-license">

<a href="https://creativecommons.org/licenses/by-sa/4.0/" rel="license"><img src="https://allthingsopen.org/wp-content/themes/ato-main-2024/img/cc/by-sa.png" title="This work is licensed under a Creative Commons Attribution-Share Alike 4.0 International License." alt="Creative Commons License" /></a>

This work is licensed under a Creative Commons Attribution-Share Alike 4.0 International License.

