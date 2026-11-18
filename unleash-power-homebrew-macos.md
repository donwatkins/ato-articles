# Unleashing the power of Homebrew on MacOS

Explore how Homebrew can search for packages, install them with a single command, list software inventory, upgrade, and more.

**By Don Watkins**  
**Published:** May 21, 2024  
**Source:** [https://allthingsopen.org/articles/unleash-power-homebrew-macos](https://allthingsopen.org/articles/unleash-power-homebrew-macos)

<figure class="featured">
<img src="https://allthingsopen.org/wp-content/uploads/2024/05/homebrew-tea-pots-e1715724485331.jpg" class="featured" alt="Different color clay tea pots" />
<figcaption>Image by <a href="https://pixabay.com/users/kittylam-2914990/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=1515579">kittylam</a> from <a href="https://pixabay.com//?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=1515579">Pixabay</a></figcaption>
</figure>

For a tech enthusiast like me, getting an M2 MacBook Air (M2 Air) isn’t just a purchase; it’s an ascent. It’s like stumbling upon a mythical unicorn, except this one runs MacOS and boasts killer battery life. While the M2 Air serves as my trusty steed, my heart still belongs to the open source realm. How can I bridge both worlds? The answer lies in Homebrew–a robust package manager for MacOS that not only simplifies installing, updating, and managing open source software, but also empowers MacOS users to unlock a whole new level of possibilities.

## The benefits of Homebrew

- **Easy installation and management of software:** Homebrew uses the familiar terminal and provides a simple way to install software using the familiar terminal, especially open source applications and developer tools. This eliminates the need to hunt down individual downloads and installers from various websites. Homebrew also streamlines the update process, allowing you to update all your installed software with a single command easily.
- **Dependency management:** Many software packages rely on other underlying software components to function correctly. Homebrew automatically takes care of these dependencies, ensuring you have everything you need installed before running the software you want. This saves you time and relieves you from potential frustrations by avoiding compatibility issues.
- **Access to a broader range of software:** While the Mac App Store offers a variety of applications, Homebrew provides a more comprehensive and much wider selection of software options, particularly developer tools and utilities that may not be available through official channels. This gives you more flexibility and control over your system.

## Installing Homebrew on MacOS

Now that we’ve highlighted the advantages of using Homebrew, let’s walk through the installation process on a MacOS system.

### **Open termina**l

Launch the terminal on your MacOS system. Navigate to `Applications > Utilities` folder or use `Spotlight` search to locate it quickly. Be sure that ‘`xcode`‘ is installed on your MacOS system. Enter the following in your terminal:

``` wp-block-prismatic-blocks
%  xcode-select --install
```

### **Install Homebrew**

Copy and paste the following command into your Terminal and press Enter:

``` wp-block-prismatic-blocks
%/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

This command initiates the Homebrew installation process.

### **Follow on-screen prompts**

The installation will guide you through the process. Follow the on-screen prompts, and you may be required to enter your system password to proceed with the installation.

### **Verify installation**

Once the installation is complete, you can verify it by running the following command:

``` wp-block-prismatic-blocks
% brew --version
```

With Homebrew successfully installed, you can now leverage its capabilities to search, manage, and install packages. Here are a few basic commands to get you started. In the screenshot below, using the` --help` option shows which commands are available.

<figure class="wp-block-image size-large">
<img src="http://allthingsopen.org/wp-content/uploads/2024/05/homebrew-1-1024x420.png" class="wp-image-5141" data-fetchpriority="high" decoding="async" srcset="https://allthingsopen.org/wp-content/uploads/2024/05/homebrew-1-1024x420.png 1024w, https://allthingsopen.org/wp-content/uploads/2024/05/homebrew-1-300x123.png 300w, https://allthingsopen.org/wp-content/uploads/2024/05/homebrew-1-768x315.png 768w, https://allthingsopen.org/wp-content/uploads/2024/05/homebrew-1-1536x630.png 1536w, https://allthingsopen.org/wp-content/uploads/2024/05/homebrew-1.png 1608w" sizes="(max-width: 1024px) 100vw, 1024px" width="1024" height="420" alt="Screenshot of the Homebrew command showing the help menu" />
<figcaption>Image by Don Watkins – CC by SA 4.0</figcaption>
</figure>

Search for packages available on Homebrew with:

``` wp-block-prismatic-blocks
% brew search inkscape
```

Install packages easily with:

``` wp-block-prismatic-blocks
% brew install inkscape
```

List the packages on the system with:

``` wp-block-prismatic-blocks
% brew list
```

<figure class="wp-block-image size-large">
<img src="http://allthingsopen.org/wp-content/uploads/2024/05/homebrew-2-1024x281.png" class="wp-image-5142" decoding="async" srcset="https://allthingsopen.org/wp-content/uploads/2024/05/homebrew-2-1024x281.png 1024w, https://allthingsopen.org/wp-content/uploads/2024/05/homebrew-2-300x82.png 300w, https://allthingsopen.org/wp-content/uploads/2024/05/homebrew-2-768x211.png 768w, https://allthingsopen.org/wp-content/uploads/2024/05/homebrew-2.png 1058w" sizes="(max-width: 1024px) 100vw, 1024px" width="1024" height="281" alt="Screenshot of the Homebrew command showing the list options" />
<figcaption>Image by Don Watkins – CC by SA 4.0</figcaption>
</figure>

It’s easy to update Homebrew with the following command:

``` wp-block-prismatic-blocks
% brew update
```

This updates Homebrew itself, but you’ll probably want to *upgrade* the open source packages you’ve installed on your MacOS system. Homebrew provides an easy way to do that by entering the following command:

``` wp-block-prismatic-blocks
% brew upgrade
```

Why settle for one world when you can embrace both? With Homebrew at your side, your M2 MacBook Air gives you access to the world of open source.

Homebrew transforms your M2 Air from a polished Apple device into a versatile open source powerhouse, letting you tap into the boundless potential of this vibrant community. You can search for packages, install them with a single command, list your software inventory, and update everything effortlessly.

</div>

---

<div class="cc-license">

<a href="https://creativecommons.org/licenses/by-sa/4.0/" rel="license"><img src="https://allthingsopen.org/wp-content/themes/ato-main-2024/img/cc/by-sa.png" title="This work is licensed under a Creative Commons Attribution-Share Alike 4.0 International License." alt="Creative Commons License" /></a>

This work is licensed under a Creative Commons Attribution-Share Alike 4.0 International License.

