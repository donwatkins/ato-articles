# Why my Podman install failed on macOS

A troubleshooting story about Homebrew, the right .dmg, and the fix that worked.

**By Don Watkins**  
**Published:** October 14, 2026  
**Source:** [https://allthingsopen.org/articles/why-my-podman-install-failed-on-macos](https://allthingsopen.org/articles/why-my-podman-install-failed-on-macos)

<figure class="featured">
<img src="https://allthingsopen.org/wp-content/uploads/2026/10/gray-seal_podman-install-e1790888737417.jpg" class="featured" alt="Gray seal laying up-side-down with red tongue sticking out" />
<figcaption>Image by <a href="https://pixabay.com/users/georg_wietschorke-3238642/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=1663712">Georg Wietschorke</a> from <a href="https://pixabay.com//?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=1663712">Pixabay</a></figcaption>
</figure>

After installing Podman on my Linux desktop and enjoying some time experimenting with containers, I was eager to set it up on my M3 MacBook Air too. Rather than following a lengthy set of instructions, I opted to install it using <a href="https://brew.sh/" target="_blank" rel="noopener">Homebrew</a>, which I did easily, since Homebrew is my go-to open source installer on macOS. However, I soon realized that the steps I’d successfully followed on my Linux Mint desktop didn’t work on macOS. Podman had been an easy Flatpak install on Linux, but something clearly worked differently here.

## When Homebrew wasn’t the answer

Frustrated with the Podman install, I turned to Docker instead, since I’d used it before and knew I could get it running on macOS. But that raised an obvious question: why would Docker run and not Podman? The missing piece, it turned out, was that I hadn’t read the excellent <a href="https://podman.io/docs" target="_blank" rel="noopener">documentation</a> on the Podman project site.

Upon reading the documentation, I discovered that my issues stemmed from an incorrect installation. Red Hat recommends installing <a href="https://podman.io/docs/installation#macos" target="_blank" rel="noopener">Podman on macOS</a> using the .dmg file instead of Homebrew. For Apple Silicon devices like mine, the best option is to use the Universal .dmg file, specifically version v1.29.1 for this install, available on their website.

After removing the Homebrew installation, I downloaded and installed it using the image file from the Podman site. Everything just worked flawlessly.

## Installing WordPress with Podman

Here are the commands I used to install WordPress on the M3:

``` wp-block-prismatic-blocks
podman pod create -n wordpress-pod -p 8080:80
```

Once the pod is created and properly mapped to port 8080, the next command sets up the MariaDB database:

``` wp-block-prismatic-blocks
podman run -d --pod wordpress-pod --name wp-db \
  -e MYSQL_ROOT_PASSWORD=mysecretpassword \
  -e MYSQL_DATABASE=wordpress \
  -e MYSQL_USER=wpuser \
  -e MYSQL_PASSWORD=mypassword \
  docker.io/library/mariadb:latest
```

Then I was ready to set up WordPress itself:

``` wp-block-prismatic-blocks
podman run -d --pod wordpress-pod --name wp-wordpress \
  -e WORDPRESS_DB_HOST=127.0.0.1:3306 \
  -e WORDPRESS_DB_USER=wpuser \
  -e WORDPRESS_DB_PASSWORD=mypassword \
  -e WORDPRESS_DB_NAME=wordpress \
  docker.io/library/wordpress:latest
```

## Finishing the WordPress setup

Once the database and the application are set up, it’s time for the first login at `http://localhost:8080`.

<div class="wp-block-image">

<figure class="aligncenter size-large">
<img src="https://allthingsopen.org/wp-content/uploads/2026/10/wordpress_language-select-737x1024.png" class="wp-image-9529" data-fetchpriority="high" decoding="async" srcset="https://allthingsopen.org/wp-content/uploads/2026/10/wordpress_language-select-737x1024.png 737w, https://allthingsopen.org/wp-content/uploads/2026/10/wordpress_language-select-216x300.png 216w, https://allthingsopen.org/wp-content/uploads/2026/10/wordpress_language-select-768x1068.png 768w, https://allthingsopen.org/wp-content/uploads/2026/10/wordpress_language-select.png 1105w" sizes="(max-width: 737px) 100vw, 737px" width="737" height="1024" alt="Wordpress on Podman language selection" />
<figcaption>Screen capture by Don Watkins CC by SA 4.0</figcaption>
</figure>

</div>

Select the correct language and click “Continue,” then set up the administrative user with a strong password (I use Bitwarden to save mine). Give the blog a name, add an email address, and you’re ready to go.

<div class="wp-block-image">

<figure class="aligncenter size-large">
<img src="https://allthingsopen.org/wp-content/uploads/2026/10/wordpress_welcome-1024x957.png" class="wp-image-9528" decoding="async" srcset="https://allthingsopen.org/wp-content/uploads/2026/10/wordpress_welcome-1024x957.png 1024w, https://allthingsopen.org/wp-content/uploads/2026/10/wordpress_welcome-300x280.png 300w, https://allthingsopen.org/wp-content/uploads/2026/10/wordpress_welcome-768x718.png 768w, https://allthingsopen.org/wp-content/uploads/2026/10/wordpress_welcome.png 1536w" sizes="(max-width: 1024px) 100vw, 1024px" width="1024" height="957" alt="Wordpress on Podman admin set-up" />
<figcaption>Screen capture by Don Watkins CC by SA 4.0</figcaption>
</figure>

</div>

Once the installation is complete, you can start blogging or just exploring WordPress.

<div class="wp-block-image">

<figure class="aligncenter size-large">
<img src="https://allthingsopen.org/wp-content/uploads/2026/10/wordpress_dashboard-1024x473.png" class="wp-image-9527" decoding="async" srcset="https://allthingsopen.org/wp-content/uploads/2026/10/wordpress_dashboard-1024x473.png 1024w, https://allthingsopen.org/wp-content/uploads/2026/10/wordpress_dashboard-300x139.png 300w, https://allthingsopen.org/wp-content/uploads/2026/10/wordpress_dashboard-768x355.png 768w, https://allthingsopen.org/wp-content/uploads/2026/10/wordpress_dashboard.png 1320w" sizes="(max-width: 1024px) 100vw, 1024px" width="1024" height="473" alt="Wordpress on Podman welcome dashboard" />
<figcaption>Screen capture by Don Watkins CC by SA 4.0</figcaption>
</figure>

</div>

## A lesson worth repeating

Following directions when diving into technical content is like following a recipe while baking a soufflé, ignore a crucial step, and you might just end up with a flat mess instead of a fluffy masterpiece.

Whether you’re installing software, setting up databases, or even assembling IKEA furniture (another exercise in patience), a little attention to the instructions can save you from hours of troubleshooting and untold frustration. When it comes to tech, “winging it” is not a strategy; it’s a fast track to panic and a mountain of confusion. There is always something to learn, even when you think you know it all.

## More from We Love Open Source

- <a href="http://allthingsopen.org/articles/15-open-source-backup-solutions-2026" target="_blank" rel="noopener">15 open source backup solutions to protect your data</a>
- <a href="https://allthingsopen.org/articles/5-common-mistakes-new-linux-users" target="_blank" rel="noopener">The 5 most common mistakes new Linux users make</a>
- <a href="https://allthingsopen.org/articles/5-linux-tools-clear-cache-remove-packages-manage-logs" target="_blank" rel="noopener">An open source alternative to AirDrop for Linux and Mac users</a>
- <a href="https://allthingsopen.org/articles/5-linux-tools-clear-cache-remove-packages-manage-logs" target="_blank" rel="noopener">5 Linux tools to clear cache, remove old packages, and manage logs</a>
- <a href="https://allthingsopen.org/articles/state-of-tech-ai-jobs-three-questions" target="_blank" rel="noopener">How has AI changed the state of tech jobs?</a>

This article is adapted from “<a href="https://donwatkins.info/2026/08/30/setting-up-podman-on-macos/" target="_blank" rel="noopener"><em>Setting up Podman on macOS</em></a>” by Don Watkins, and is republished with permission from the author.

</div>

---

<div class="cc-license">

<a href="https://creativecommons.org/licenses/by-sa/4.0/" rel="license"><img src="https://allthingsopen.org/wp-content/themes/ato-main-2024/img/cc/by-sa.png" title="This work is licensed under a Creative Commons Attribution-Share Alike 4.0 International License." alt="Creative Commons License" /></a>

This work is licensed under a Creative Commons Attribution-Share Alike 4.0 International License.

