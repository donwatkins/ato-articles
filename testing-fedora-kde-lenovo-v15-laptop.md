# Exploring Fedora KDE on a new Lenovo laptop

My experience running Linux on the Lenovo V15.

**By Don Watkins**  
**Published:** June 2, 2025  
**Source:** [https://allthingsopen.org/articles/testing-fedora-kde-lenovo-v15-laptop](https://allthingsopen.org/articles/testing-fedora-kde-lenovo-v15-laptop)

<figure class="featured">
<img src="https://allthingsopen.org/wp-content/uploads/2024/11/computer-usb-thumbdrive-e1730742549828.jpg" class="featured" alt="Removable laptop media USB thumbdrive" />
<figcaption>Image by <a href="https://pixabay.com/users/skitterphoto-324082/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=2786081">Rudy and Peter Skitterians</a> from <a href="https://pixabay.com//?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=2786081">Pixabay</a></figcaption>
</figure>

I’d been nursing an old laptop for a while, long enough that the missing “P” key started to feel like a personality quirk. But once I realized fixing it would take more effort than I wanted to give, I began shopping for a replacement.

A few weeks ago, while helping a friend set up her new machine, the staff at a local store suggested I look at the Lenovo V15. It had the specs I needed (Ryzen 7 CPU, 16 GB of RAM, 512 GB NVMe drive) and the price was right. But I had one big question: Would it play nice with Linux?

## What to expect when installing Fedora KDE on the Lenovo V15

I’ve been running <a href="http://allthingsopen.org/articles/top-5-fedora-kde-plasma-apps" target="_blank" rel="noreferrer noopener">Fedora KDE Plasma</a> since January and didn’t want to give that up. After finding very little online about Linux compatibility with this exact model, I decided to take the plunge anyway.

I bought the machine from BJs.com. It shipped with Windows 11 Home, which I immediately replaced with Fedora 42 KDE Plasma using a <a href="http://allthingsopen.org/articles/dd-command-bootable-linux-drives" target="_blank" rel="noreferrer noopener">USB stick</a>. I’m happy to report: It works beautifully.

**Read more: <a href="http://allthingsopen.org/articles/ventoy-how-to-build-multi-distribution-linux-usb-drive" target="_blank" rel="noreferrer noopener">How to quickly build a multi-distribution Linux USB drive</a>**

## Performance and compatibility

This is my first Lenovo, and I’ve been impressed. The keyboard is responsive and yes, the “P” key works! Installing the `inxi` tool gives a nice look under the hood (see complete [output below](https://allthingsopen.org/articles/testing-fedora-kde-lenovo-v15-laptop#inxi)).

- **CPU:** AMD Ryzen 7 7730U (8-core)
- **Graphics:** AMD Radeon with full OpenGL support via Mesa drivers
- **Networking:** Realtek wireless and Ethernet both worked without issue

## Design and daily use

The Lenovo V15 is lightweight, listed at 3.64 pounds but feels even lighter. The plastic build is sturdy enough for everyday use and daily tasks. The display is more than adequate for writing, browsing, and streaming.

I mostly use a Logitech M325 wireless mouse, and the touchpad is decent, I just don’t use it often. KDE Plasma offers plenty of options for fine-tuning it, which I may explore more later.

I’ve been particularly impressed by the Realtek 802.11ax wireless, it’s been stable and fast. I like that the machine also includes an Ethernet port, a must-have when helping friends troubleshoot flaky connections.

## Ports and expandability

The Lenovo V15 includes:

- 2 USB-A ports
- 1 USB-C port
- 1 HDMI port
- 1 headphone jack
- 1 Ethernet port

I verified the machine internals with `inxi` (see [output below](https://allthingsopen.org/articles/testing-fedora-kde-lenovo-v15-laptop#inxi)).

**Read more: <a href="http://allthingsopen.org/articles/top-5-fedora-kde-plasma-apps" target="_blank" rel="noreferrer noopener">My top 5 must-have apps on Fedora 41 KDE Plasma</a>**

If you’re a Linux user looking for a budget-friendly, lightweight laptop that plays well with distributions like Fedora KDE Plasma, the Lenovo V15 is a great option. I’m happy with the hardware and wanted to share my experience for anyone searching for a solid laptop that runs their favorite Linux distro without hassle. Hopefully, this post helps someone else on the same search.

## More from We Love Open Source

- <a href="http://allthingsopen.org/articles/top-5-fedora-kde-plasma-apps" target="_blank" rel="noreferrer noopener">My top 5 must-have apps on Fedora 41 KDE Plasma</a>
- <a href="http://allthingsopen.org/articles/ventoy-how-to-build-multi-distribution-linux-usb-drive" target="_blank" rel="noreferrer noopener">How to quickly build a multi-distribution Linux USB drive</a>
- <a href="http://allthingsopen.org/articles/10-sysadmin-networking-commands" target="_blank" rel="noreferrer noopener">10 essential networking commands for sysadmins</a>
- <a href="http://allthingsopen.org/articles/10-free-open-source-tools-work-privacy-creativity" target="_blank" rel="noreferrer noopener">10 open source tools you can start using today</a>
- <a href="http://allthingsopen.org/articles/what-is-opentelemetry-add-django-application" target="_blank" rel="noreferrer noopener">What is OpenTelemetry?</a>

This article is adapted from “[*Lenovo V15 & Linux: A Perfect Match? My Fedora KDE Plasma Experience*](https://donwatkins.info/2025/05/09/lenovo-v15-linux-a-perfect-match-my-fedora-kde-plasma-experience/)” by Don Watkins, and is republished with permission from the author.

### `inxi` output

``` wp-block-prismatic-blocks
System:
    Kernel: 6.14.5-300.fc42.x86_64 arch: x86_64 bits: 64
  Desktop: KDE Plasma v: 6.3.5 Distro: Fedora Linux 42 (KDE Plasma Desktop
    Edition)
Machine:
  Type: Laptop System: LENOVO product: 82YY v: Lenovo V15 G4 ABP
    serial: <superuser required>
  Mobo: LENOVO model: LNVNB161216 v: SDK0T76463WIN
    serial: <superuser required> UEFI: LENOVO v: MSCN17WW date: 08/08/2024
Battery:
  ID-1: BAT0 charge: 25.5 Wh (65.4%) condition: 39.0/38.0 Wh (102.5%)
    volts: 7.9 min: 7.7
CPU:
  Info: 8-core AMD Ryzen 7 7730U with Radeon Graphics [MT MCP] speed (MHz):
    avg: 1397 min/max: 400/4547
Graphics:
  Device-1: Advanced Micro Devices [AMD/ATI] Barcelo driver: amdgpu v: kernel
  Device-2: Bison Integrated Camera driver: uvcvideo type: USB
  Display: wayland server: Xwayland v: 24.1.6 compositor: kwin_wayland
    driver: gpu: amdgpu resolution: 1920x1080~60Hz
  API: OpenGL v: 4.6 compat-v: 4.5 vendor: amd mesa v: 25.0.4 renderer: AMD
    Radeon Graphics (radeonsi renoir ACO DRM 3.61 6.14.5-300.fc42.x86_64)
  Info: Tools: api: clinfo, eglinfo, glxinfo, vulkaninfo
    de: kscreen-console,kscreen-doctor wl: wayland-info x11: xdriinfo,
    xdpyinfo, xprop, xrandr
Network:
  Device-1: Realtek RTL8111/8168/8211/8411 PCI Express Gigabit Ethernet
    driver: r8169
  Device-2: Realtek RTL8852BE PCIe 802.11ax Wireless Network
    driver: rtw89_8852be
Drives:
  Local Storage: total: 476.94 GiB used: 6.07 GiB (1.3%)
Info:
  Memory: total: 16 GiB note: est. available: 13.48 GiB used: 3.88 GiB (28.8%)
  Processes: 371 Uptime: 1h 21m Shell: Bash inxi: 3.3.38
```

</div>

---

<div class="cc-license">

<a href="https://creativecommons.org/licenses/by-sa/4.0/" rel="license"><img src="https://allthingsopen.org/wp-content/themes/ato-main-2024/img/cc/by-sa.png" title="This work is licensed under a Creative Commons Attribution-Share Alike 4.0 International License." alt="Creative Commons License" /></a>

This work is licensed under a Creative Commons Attribution-Share Alike 4.0 International License.

