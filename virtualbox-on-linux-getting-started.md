# Getting started with VirtualBox on Linux: From hobbyist tinkering to production prep

See how you can test new environments safely without risking your production setup.

**By Don Watkins**  
**Published:** December 3, 2025  
**Source:** [https://allthingsopen.org/articles/virtualbox-on-linux-getting-started](https://allthingsopen.org/articles/virtualbox-on-linux-getting-started)

<figure class="featured">
<img src="https://allthingsopen.org/wp-content/uploads/2025/11/laptop-virtual-computer-e1763657052199.jpg" class="featured" alt="Silver laptop on a dark table with neat, organized storage in the background" />
<figcaption>Image by <a href="https://pixabay.com/users/pexels-2286921/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=1846277">Pexels</a> from <a href="https://pixabay.com//?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=1846277">Pixabay</a></figcaption>
</figure>

I started using VirtualBox many years ago, and it quickly became my go-to virtualization platform. What drew me in first was its open source foundation. The base package, source code and binaries included, is licensed under [GPLv3](https://www.virtualbox.org/wiki/Licensing_FAQ), making it a transparent and accessible option for anyone exploring virtual machines.

<a href="https://www.virtualbox.org/" target="_blank" rel="noreferrer noopener">VirtualBox</a> is also remarkably versatile. It runs on Linux, macOS (Intel and ARM), Windows, and even Solaris. Since its initial release in 2007, it has enjoyed continuous development, with steady improvements and frequent updates. The latest stable version, 7.2.4, shipped in October, a clear sign that the project remains active and evolving.

For me, though, VirtualBox is more than a piece of software. It’s a sandbox for learning and experimentation. I use it to test new Linux distributions, try out fresh Windows releases, and occasionally help others troubleshoot or validate configurations before deploying them in the real world.

**Read more: <a href="http://allthingsopen.org/articles/12-everyday-technologies-powered-by-linux" target="_blank" rel="noreferrer noopener">12 everyday technologies powered by Linux</a>**

## My daily driver setup

To put my workflow in context, my main workstation is a System76 <a href="https://system76.com/desktops/meerkat/" target="_blank" rel="noreferrer noopener">Meerkat</a> running Linux Mint 22.2. With 32 GB of RAM and a one-terabyte NVMe drive, it’s a compact but powerful machine. Virtualization is effortless on this setup; I can run multiple virtual machines with no noticeable slowdown thanks to the generous memory and fast storage.

Installing VirtualBox on Linux Mint is straightforward:

``` wp-block-prismatic-blocks
$ sudo apt install virtualbox
```

And for Fedora users:

``` wp-block-prismatic-blocks
$ sudo dnf install virtualbox
```

Within minutes, you can have a fully functional virtualization environment ready for whatever OS you want to explore.

**Read more: <a href="http://allthingsopen.org/articles/10-free-open-source-tools-work-privacy-creativity" target="_blank" rel="noreferrer noopener">10 open source tools you can start using today</a>**

## The dreaded VT-x error

Of course, not every moment is smooth sailing. When I first ran VirtualBox on my Linux Mint system, I hit a frustrating error:

``` wp-block-prismatic-blocks
VT-x is being used by another hypervisor (VERR_VMX_IN_VMX_ROOT_MODE).
VirtualBox can't operate in VMX root mode. Please disable the KVM kernel extension,
recompile your kernel and reboot (VERR_VMX_IN_VMX_ROOT_MODE).
```

It looks alarming, but the explanation is simple: Another hypervisor, in this case, KVM, is already using the VT-x virtualization extensions. Because both KVM and VirtualBox require VT-x, they can’t run simultaneously.

## The fix: disabling KVM

Fortunately, the solution is quick. After a bit of searching, I found that unloading the KVM Intel kernel module frees up the virtualization extensions:

``` wp-block-prismatic-blocks
$ sudo modprobe -r kvm_intel
```

Once I ran that command, VirtualBox started without any issues. No kernel recompilation, no reboot required. This trick is now part of my routine whenever the VT-x error appears.

## A real-world use case: Helping my dentist

One example shows just how practical VirtualBox can be. My dentist needed help setting up a Windows Server 2025 file server for his practice management system. Rather than risking changes on his production hardware, I spun up a test environment in VirtualBox. This allowed me to configure and validate everything safely before deploying it for real.

That flexibility is one of VirtualBox’s greatest strengths. You can simulate complex environments without extra equipment, expense, or risk, which is useful whether you’re a hobbyist tinkering with operating systems or a professional preparing for a production rollout.

## Building a Windows Server test environment

I downloaded the <a href="https://info.microsoft.com/ww-landing-evaluate-windows-server-2025.html" target="_blank" rel="noreferrer noopener">Windows Server 2025 evaluation ISO</a> from Microsoft (about 5 GB) and mounted it in VirtualBox as the installation media.

<div class="wp-block-image">

<figure class="aligncenter size-full">
<img src="http://allthingsopen.org/wp-content/uploads/2025/11/ServerSetup.png" class="wp-image-8028" data-fetchpriority="high" decoding="async" srcset="https://allthingsopen.org/wp-content/uploads/2025/11/ServerSetup.png 1016w, https://allthingsopen.org/wp-content/uploads/2025/11/ServerSetup-300x146.png 300w, https://allthingsopen.org/wp-content/uploads/2025/11/ServerSetup-768x373.png 768w" sizes="(max-width: 1016px) 100vw, 1016px" width="1016" height="494" alt="Windows Server 2025 ISO from Microsoft VirtualBox setup" />
<figcaption>Screen capture by Don Watkins, CC-BY-SA 4.0</figcaption>
</figure>

</div>

From there, I used VirtualBox’s built-in tools to configure storage and networking. The default 50 GB virtual disk worked fine for testing, though you can expand the size or attach additional drives if you want to explore more advanced layouts. I selected a bridged network adapter so the VM could communicate on my home network just like any other system. VirtualBox doesn’t support hardware RAID, but software RAID is perfectly workable for experimentation.

<div class="wp-block-image">

<figure class="aligncenter size-full">
<img src="http://allthingsopen.org/wp-content/uploads/2025/11/storage.png" class="wp-image-8027" decoding="async" srcset="https://allthingsopen.org/wp-content/uploads/2025/11/storage.png 936w, https://allthingsopen.org/wp-content/uploads/2025/11/storage-300x156.png 300w, https://allthingsopen.org/wp-content/uploads/2025/11/storage-768x400.png 768w" sizes="(max-width: 936px) 100vw, 936px" width="936" height="488" alt="VirtualBox storage options" />
<figcaption>Screen capture by Don Watkins, CC-BY-SA 4.0</figcaption>
</figure>

</div>

With the preliminary configuration done, I launched the VM and began the Windows Server installation. The process mirrors installing on physical hardware, though it runs noticeably faster in a virtual environment.

<div class="wp-block-image">

<figure class="aligncenter size-full">
<img src="http://allthingsopen.org/wp-content/uploads/2025/11/ServerStartUp.png" class="wp-image-8026" decoding="async" srcset="https://allthingsopen.org/wp-content/uploads/2025/11/ServerStartUp.png 768w, https://allthingsopen.org/wp-content/uploads/2025/11/ServerStartUp-300x241.png 300w" sizes="(max-width: 768px) 100vw, 768px" width="768" height="617" alt="VirtualBox server startup" />
<figcaption>Screen capture by Don Watkins, CC-BY-SA 4.0</figcaption>
</figure>

</div>

When everything finished, I had a clean Windows Server 2025 instance ready to explore. Testing each configuration in VirtualBox made the eventual real-world deployment far smoother and eliminated the risk of breaking my dentist’s production setup.

<div class="wp-block-image">

<figure class="aligncenter size-full">
<img src="http://allthingsopen.org/wp-content/uploads/2025/11/Server2025Running.png" class="wp-image-8025" decoding="async" srcset="https://allthingsopen.org/wp-content/uploads/2025/11/Server2025Running.png 768w, https://allthingsopen.org/wp-content/uploads/2025/11/Server2025Running-300x238.png 300w" sizes="(max-width: 768px) 100vw, 768px" width="768" height="610" alt="VirtualBox 2025 running server" />
<figcaption>Screen capture by Don Watkins, CC-BY-SA 4.0</figcaption>
</figure>

</div>

## Final thoughts

My journey with VirtualBox has been one of exploration, learning, and practical utility. Whether I’m testing a new Linux distro or helping my dentist prep a Windows Server, VirtualBox consistently delivers a reliable and flexible environment.

If you’ve never tried VirtualBox, it’s absolutely worth exploring. Whether you’re on Linux, macOS, Windows, or Solaris, it offers a safe, powerful way to experiment and build your skills in the digital world.

## More from We Love Open Source

- <a href="http://allthingsopen.org/articles/12-everyday-technologies-powered-by-linux" target="_blank" rel="noreferrer noopener">12 everyday technologies powered by Linux</a>
- <a href="http://allthingsopen.org/articles/testing-fedora-kde-lenovo-v15-laptop" target="_blank" rel="noreferrer noopener">Exploring Fedora KDE on a new Lenovo laptop</a>
- <a href="http://allthingsopen.org/articles/10-sysadmin-networking-commands" target="_blank" rel="noreferrer noopener">10 essential networking commands for sysadmins</a>
- <a href="http://allthingsopen.org/articles/how-to-linux-ready-hardware-compatibility" target="_blank" rel="noreferrer noopener">Linux-ready hardware: What to look for before you buy</a>
- <a href="http://allthingsopen.org/articles/10-free-open-source-tools-work-privacy-creativity" target="_blank" rel="noreferrer noopener">10 open source tools you can start using today</a>

This article is adapted from “*<a href="https://donwatkins.info/2025/11/14/virtualbox-a-longtime-companion-in-my-tech-journey/" target="_blank" rel="noreferrer noopener">VirtualBox: A longtime companion in my tech journey</a>*” by Don Watkins, and is republished with permission from the author.

</div>

---

<div class="cc-license">

<a href="https://creativecommons.org/licenses/by-sa/4.0/" rel="license"><img src="https://allthingsopen.org/wp-content/themes/ato-main-2024/img/cc/by-sa.png" title="This work is licensed under a Creative Commons Attribution-Share Alike 4.0 International License." alt="Creative Commons License" /></a>

This work is licensed under a Creative Commons Attribution-Share Alike 4.0 International License.

