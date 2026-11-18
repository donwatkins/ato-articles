# How to quickly build a multi-distribution Linux USB drive with Ventoy

Try this open source tool that lets you carry multiple Linux distros on a single thumb drive.

**By Don Watkins**  
**Published:** February 20, 2025  
**Source:** [https://allthingsopen.org/articles/ventoy-how-to-build-multi-distribution-linux-usb-drive](https://allthingsopen.org/articles/ventoy-how-to-build-multi-distribution-linux-usb-drive)

<figure class="featured">
<img src="https://allthingsopen.org/wp-content/uploads/2024/11/computer-usb-thumbdrive-e1730742549828.jpg" class="featured" alt="Removable laptop media USB thumbdrive" />
<figcaption>Image by <a href="https://pixabay.com/users/skitterphoto-324082/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=2786081">Rudy and Peter Skitterians</a> from <a href="https://pixabay.com//?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=2786081">Pixabay</a></figcaption>
</figure>

Giving friends and neighbors a bootable USB drive containing your favorite Linux distribution is a great way to introduce neophyte Linux users to the experience we all enjoy. Many people have never heard of Linux, and putting your favorite distribution on a bootable USB drive is a great way to break the ice.

I taught an introductory computer class to a group of middle schoolers a few years ago. We used old laptops, and I introduced the students to Fedora, Ubuntu, and Pop!\_OS. When the class was over, I gave each student a copy of their favorite distribution to take home and install on a computer of their choice. They were eager to try their new skills at home.

A friend introduced me to <a href="https://www.ventoy.net/" target="_blank" rel="noreferrer noopener">Ventoy</a>, which (according to its GitHub repository) is “an open source tool to create bootable a USB drive for ISO/WIM/IMG/VHD(x)/EFI files.” Instead of creating separate drives for each Linux distribution I want to share, I can make a single drive with *all* my favorite Linux distributions on the drive!

As you might expect, a USB drive’s size determines how many distributions you can fit on it. On a 16GB drive, I placed Fedora Cinnamon and Fedora KDE Plasma and still have over nine gigabytes free to hold other distributions.

## Getting started with Ventoy

Ventoy is open source, with a <a href="https://www.ventoy.net/en/doc_license.html" target="_blank" rel="noreferrer noopener">GPL v3</a> license, and available for Windows and Linux. There is excellent <a href="https://www.ventoy.net/en/doc_news.html" target="_blank" rel="noreferrer noopener">documentation</a> on downloading and installing Ventoy on Microsoft Windows. The Linux installation happens from the command line, so it can be a little confusing if you’re unfamiliar with that process. Yet, it’s easier than it might seem.

First, <a href="https://github.com/ventoy/Ventoy/releases" target="_blank" rel="noreferrer noopener">download Ventoy</a>. I downloaded the archive file to my desktop. Next, extract the `ventoy-x.y.z-linux.tar.gz` archive (but replace `x.y.z` with your download’s version number) using the `tar` command (to keep things simple, I use the `*` character as an infinite wildcard in the command):

``` wp-block-prismatic-blocks
$ tar -xvf ventoy*z
```

This command extracts (unzips) all the necessary files into a folder named `ventoy-x.y.z` on my desktop.

You can also use your Linux distribution’s archive manager to accomplish the same task. After downloading and extracting, you can install Ventoy to your USB drive.

**Read more: <a href="http://allthingsopen.org/articles/dd-command-bootable-linux-drives" target="_blank" rel="noreferrer noopener">How to use the dd command to create bootable Linux drives</a>**

## Install Ventoy and Linux on a USB

Insert your USB drive into your computer. Change the directory into the Ventoy folder, and look for a shell script named `Ventoy2Disk.sh`. For this script to work correctly, you must determine the correct mount point for your USB drive.

``` wp-block-prismatic-blocks
$ lsblk
```

The results show that my USB drive is mounted at `/dev/sda`. On your computer, the location could be `/dev/sdb` or `/dev/sdc` or something similar.

Once you’re sure of your drive’s location, run the following script, where `X` is the drive location:

``` wp-block-prismatic-blocks
$ sudo sh Ventoy2Disk.sh -i /dev/sdX
```

This formats the drive and installs Ventoy to your USB. Now, you can copy and paste all the Linux distributions that will fit on the drive. If you boot the newly created drive on your computer, you’ll see a menu with the distributions you have copied to your USB drive.

**Read more: <a href="http://allthingsopen.org/articles/discover-system-information-inxi" target="_blank" rel="noreferrer noopener">Discovering system information with inxi</a>**

## Build a portable powerhouse

<div class="wp-block-image">

<figure class="aligncenter size-full">
<img src="http://allthingsopen.org/wp-content/uploads/2025/02/ventoy_boot.jpg" class="wp-image-6614" data-fetchpriority="high" decoding="async" srcset="https://allthingsopen.org/wp-content/uploads/2025/02/ventoy_boot.jpg 768w, https://allthingsopen.org/wp-content/uploads/2025/02/ventoy_boot-300x225.jpg 300w" sizes="(max-width: 768px) 100vw, 768px" width="768" height="576" alt="Picture of a Dell laptop displaying the Ventoy boot sequence screen." />
<figcaption>Photo by Don Watkins, CC-BY-SA 4.0</figcaption>
</figure>

</div>

Ventoy is your key to carrying a multiboot drive on your keychain, so you’ll never be without the distributions you rely on. You can have a full-featured desktop, a lightweight distro, a console-only maintenance utility, *and* anything else you want.

I never leave the house without a Linux distro, nor should you. Grab Ventoy, a USB drive, and a handful of ISOs. You won’t be sorry.

## More from We Love Open Source

- <a href="http://allthingsopen.org/articles/dd-command-bootable-linux-drives" target="_blank" rel="noreferrer noopener">How to use the dd command to create bootable Linux drives</a>
- <a href="http://allthingsopen.org/articles/getting-started-llamafile-tutorial" target="_blank" rel="noreferrer noopener">Getting started with Llamafile tutorial</a>
- <a href="http://allthingsopen.org/articles/discover-system-information-inxi" target="_blank" rel="noreferrer noopener">Discovering system information with inxi</a>
- <a href="http://allthingsopen.org/articles/enhance-writing-skills-ollama-phi3" target="_blank" rel="noreferrer noopener">Enhance your writing skills with Ollama and Phi3</a>

This article is adapted from “*<a href="https://donwatkins.info/2025/02/13/ventoy-the-ultimate-multi-boot-usb-tool/" target="_blank" rel="noreferrer noopener">Ventoy: The ultimate multi-boot USB tool</a>*” by Don Watkins, and is republished with permission from the author.

</div>

---

<div class="cc-license">

<a href="https://creativecommons.org/licenses/by-sa/4.0/" rel="license"><img src="https://allthingsopen.org/wp-content/themes/ato-main-2024/img/cc/by-sa.png" title="This work is licensed under a Creative Commons Attribution-Share Alike 4.0 International License." alt="Creative Commons License" /></a>

This work is licensed under a Creative Commons Attribution-Share Alike 4.0 International License.

