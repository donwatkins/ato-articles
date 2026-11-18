# QGIS meets mobile: A practical guide to field mapping with MerginMaps

Create, sync, and manage geospatial projects across desktop and mobile devices with open source tools.

**By Don Watkins**  
**Published:** March 4, 2026  
**Source:** [https://allthingsopen.org/articles/qgis-mobile-field-mapping-merginmaps](https://allthingsopen.org/articles/qgis-mobile-field-mapping-merginmaps)

<figure class="featured">
<img src="https://allthingsopen.org/wp-content/uploads/2026/02/gis-map-phone-e1771271527244.jpg" class="featured" alt="Mobile phone on top of a map of the world" />
<figcaption>Image by <a href="https://pixabay.com/users/pexels-2286921/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=1869510">Pexels</a> from <a href="https://pixabay.com//?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=1869510">Pixabay</a></figcaption>
</figure>

Recently a friend asked me if I could help him map his walks around the area where he lives. I use a pedometer to track my steps and have tried several different map walking apps on my phone and smartwatch. I told my friend I would do some research and get back to him.

Later that day, using AI, I found about a half dozen mapping applications. <a href="https://qgis.org/" id="https://qgis.org/" type="link" target="_blank" rel="noreferrer noopener">QGIS</a> caught my eye because it’s open source. I decided to give it a try and install it on my Linux computer using the Flatpak installation, which was the easiest option on Linux Mint.

## **Installing QGIS**

``` wp-block-prismatic-blocks
$ flatpak install flathub org.qgis.qgis
```

You will be prompted for the version of QGIS you want to use and the app should appear in your application launcher. QGIS has excellent <a href="https://qgis.org/resources/installation-guide/" id="https://qgis.org/resources/installation-guide/" type="link" target="_blank" rel="noreferrer noopener">documentation</a> and can be installed on nearly any of the popular computing platforms including macOS, Windows, Linux, FreeBSD, OpenBSD and even as container images.

## **First impressions**

Once I launched the application, I was presented with an incredibly complex toolset. QGIS allows users to create, edit, visualize, analyze, and publish geospatial data. It supports various data formats—including vector, raster, and database formats—and provides tools for creating maps, performing spatial queries, and generating reports. I simply wanted to create trail maps and count steps for my friend.

<div class="wp-block-image">

<figure class="aligncenter size-large">
<img src="http://allthingsopen.org/wp-content/uploads/2026/02/QGIS-1024x496.png" class="wp-image-8498" data-fetchpriority="high" decoding="async" srcset="https://allthingsopen.org/wp-content/uploads/2026/02/QGIS-1024x496.png 1024w, https://allthingsopen.org/wp-content/uploads/2026/02/QGIS-300x145.png 300w, https://allthingsopen.org/wp-content/uploads/2026/02/QGIS-768x372.png 768w, https://allthingsopen.org/wp-content/uploads/2026/02/QGIS.png 1438w" sizes="(max-width: 1024px) 100vw, 1024px" width="1024" height="496" alt="GQIS user interface" />
<figcaption>Screen capture by Don Watkins CC by SA 4.0</figcaption>
</figure>

</div>

A <a href="https://mapscaping.com/podcast/qgis-an-opensource-geospatial-project/" id="https://mapscaping.com/podcast/qgis-an-opensource-geospatial-project/" type="link" target="_blank" rel="noreferrer noopener">podcast</a> gave me a good overview of QGIS—it’s open source (GPL v2), released in 2002, and extended with over 1,300 <a href="https://plugins.qgis.org/plugins/" id="https://plugins.qgis.org/plugins/" type="link" target="_blank" rel="noreferrer noopener">plugins</a>. I’m using version 3.44 “Solothurn.” Which plugins would I need to map the trails at the retreat center where my friend lives?

**Read more: <a href="http://allthingsopen.org/articles/system76-meerkat-linux-developer-workstation" id="8422" type="articles" target="_blank" rel="noreferrer noopener">Meet the Meerkat: A compact Linux PC</a>**

## **Setting up the essential plugins**

The first plugin I installed was <a href="https://plugins.qgis.org/plugins/quick_map_services/" id="https://plugins.qgis.org/plugins/quick_map_services/" type="link" target="_blank" rel="noreferrer noopener">Quick Map Services</a>, which allowed me to download Open Street Map. Now I had some data, but how could I use it?

With more help from my AI app, I discovered <a href="https://merginmaps.com/" id="https://merginmaps.com/" type="link" target="_blank" rel="noreferrer noopener">MerginMaps</a>—a plugin that extends QGIS. They have an app for iOS and Android, so I could use my mobile phone for data collection. MerginMaps is open source, including the mobile app!

To get started, I needed to install the MerginMaps plugin in QGIS first. Go to ‘Plugins’ on the menu bar at the top and select ‘Manage and Install Plugins.’ Use the ‘Search’ window to search for ‘MerginMaps.’

<div class="wp-block-image">

<figure class="aligncenter size-large">
<img src="http://allthingsopen.org/wp-content/uploads/2026/02/mergin-maps-1024x750.png" class="wp-image-8487" decoding="async" srcset="https://allthingsopen.org/wp-content/uploads/2026/02/mergin-maps-1024x750.png 1024w, https://allthingsopen.org/wp-content/uploads/2026/02/mergin-maps-300x220.png 300w, https://allthingsopen.org/wp-content/uploads/2026/02/mergin-maps-768x562.png 768w, https://allthingsopen.org/wp-content/uploads/2026/02/mergin-maps.png 1101w" sizes="(max-width: 1024px) 100vw, 1024px" width="1024" height="750" alt="MerginMaps QGIS program" />
<figcaption>Screen capture by Don Watkins CC by SA 4.0</figcaption>
</figure>

</div>

At the bottom of the window is a button to ‘Install Plugin’. Once the plugin is installed, you’re ready to connect MerginMaps with QGIS. I also needed to install MerginMaps on my iPhone and create a MerginMaps account—you’ll need an account to use the plugin.

<div class="wp-block-image">

<figure class="aligncenter size-large">
<img src="http://allthingsopen.org/wp-content/uploads/2026/02/mergin-account-1024x425.png" class="wp-image-8488" decoding="async" srcset="https://allthingsopen.org/wp-content/uploads/2026/02/mergin-account-1024x425.png 1024w, https://allthingsopen.org/wp-content/uploads/2026/02/mergin-account-300x125.png 300w, https://allthingsopen.org/wp-content/uploads/2026/02/mergin-account-768x319.png 768w, https://allthingsopen.org/wp-content/uploads/2026/02/mergin-account.png 1530w" sizes="(max-width: 1024px) 100vw, 1024px" width="1024" height="425" alt="MerginMaps account create" />
<figcaption>Screen capture by Don Watkins CC by SA 4.0</figcaption>
</figure>

</div>

## **Configuring MerginMaps**

Next, sign into your MerginMaps account in QGIS. When you installed the MerginMaps plugin, it altered your menu options slightly. The arrow in the screenshot points to the Mergin menu options. The second item that looks like a gear is where you sign in to Mergin—that’s the configure button.

<div class="wp-block-image">

<figure class="aligncenter size-full">
<img src="http://allthingsopen.org/wp-content/uploads/2026/02/mergin-menu.png" class="wp-image-8489" decoding="async" srcset="https://allthingsopen.org/wp-content/uploads/2026/02/mergin-menu.png 768w, https://allthingsopen.org/wp-content/uploads/2026/02/mergin-menu-300x60.png 300w" sizes="(max-width: 768px) 100vw, 768px" width="768" height="154" alt="MerginMaps menu" />
<figcaption>Screen capture by Don Watkins CC by SA 4.0</figcaption>
</figure>

</div>

Click that button and you’ll be prompted to sign in to MerginMaps.

<div class="wp-block-image">

<figure class="aligncenter size-full">
<img src="http://allthingsopen.org/wp-content/uploads/2026/02/mergin_sign-in.png" class="wp-image-8490" decoding="async" srcset="https://allthingsopen.org/wp-content/uploads/2026/02/mergin_sign-in.png 768w, https://allthingsopen.org/wp-content/uploads/2026/02/mergin_sign-in-300x118.png 300w" sizes="(max-width: 768px) 100vw, 768px" width="768" height="302" alt="MerginMaps sign-in" />
<figcaption>Screen capture by Don Watkins CC by SA 4.0</figcaption>
</figure>

</div>

## **Creating your first project**

Once you have signed into MerginMaps you can begin your first project. Next to the gear like ‘Configure’ button is another button with a plus sign on it. Clicking on that brings up a ‘New basic QGIS project’ option.

<div class="wp-block-image">

<figure class="aligncenter size-full">
<img src="http://allthingsopen.org/wp-content/uploads/2026/02/new-map-project.png" class="wp-image-8491" decoding="async" srcset="https://allthingsopen.org/wp-content/uploads/2026/02/new-map-project.png 756w, https://allthingsopen.org/wp-content/uploads/2026/02/new-map-project-300x234.png 300w" sizes="(max-width: 756px) 100vw, 756px" width="756" height="589" alt="Creating a new project within MerginMaps in QGIS" />
<figcaption>Screen capture by Don Watkins CC by SA 4.0</figcaption>
</figure>

</div>

After creating the new project, you’re invited to give it a name. Once named, the project is immediately uploaded to the MerginMaps server and saved locally in a directory location of your choosing.

<div class="wp-block-image">

<figure class="aligncenter size-full">
<img src="http://allthingsopen.org/wp-content/uploads/2026/02/newproject.png" class="wp-image-8492" decoding="async" srcset="https://allthingsopen.org/wp-content/uploads/2026/02/newproject.png 750w, https://allthingsopen.org/wp-content/uploads/2026/02/newproject-300x233.png 300w" sizes="(max-width: 750px) 100vw, 750px" width="750" height="582" alt="Saving a new project within MerginMaps in QGIS" />
<figcaption>Screen capture by Don Watkins CC by SA 4.0</figcaption>
</figure>

</div>

## **Mobile field data collection**

After the project is uploaded to the MerginMaps server, it’s time to get out your iOS or Android device. Sign in to the MerginMaps server and download the project onto your mobile device. At the bottom of the application window, there’s a ‘Projects’ button that provides a listing of the projects on your device.

<div class="wp-block-image">

<figure class="aligncenter size-full">
<img src="http://allthingsopen.org/wp-content/uploads/2026/02/projects.jpg" class="wp-image-8493" decoding="async" srcset="https://allthingsopen.org/wp-content/uploads/2026/02/projects.jpg 475w, https://allthingsopen.org/wp-content/uploads/2026/02/projects-139x300.jpg 139w" sizes="(max-width: 475px) 100vw, 475px" width="475" height="1024" alt="MerginMaps iOS application window" />
<figcaption>Screen capture by Don Watkins CC by SA 4.0</figcaption>
</figure>

</div>

## **Testing in the field**

I decided to give the application a test run by mapping points on my daily walk around the village. I created a MerginMaps project in QGIS and uploaded it to the server, then downloaded the project onto my iPhone and set off around the village.

Once the data points are collected on the device, they can be uploaded to the MerginMaps server and then downloaded to the QGIS software on your computer to generate maps. Here’s a map of my walk in Franklinville, New York.

<div class="wp-block-image">

<figure class="aligncenter size-full">
<img src="http://allthingsopen.org/wp-content/uploads/2026/02/FranklinvilleMap-768x682-1.png" class="wp-image-8494" decoding="async" srcset="https://allthingsopen.org/wp-content/uploads/2026/02/FranklinvilleMap-768x682-1.png 768w, https://allthingsopen.org/wp-content/uploads/2026/02/FranklinvilleMap-768x682-1-300x266.png 300w" sizes="(max-width: 768px) 100vw, 768px" width="768" height="682" alt="Map of the Village of Franklinville New York generated in conjunction with MerginMap and QGIS." />
<figcaption>Screen capture by Don Watkins CC by SA 4.0</figcaption>
</figure>

</div>

## **Conclusion**

QGIS and MerginMaps offer a powerful combination for field mapping. Together, they provide a robust solution for mapping trails, making it easier for my friend—and anyone else—to do the same. The integration highlights the potential of open source tools for geospatial work, whether for individual use or team-based projects.

The tools are free, powerful, and accessible across multiple platforms. Whether you’re mapping retreat center trails, documenting neighborhood walks, or conducting field research, this open source combination makes professional-grade mapping accessible to everyone.

## More from We Love Open Source

- <a href="http://allthingsopen.org/articles/15-open-source-backup-solutions-2026" target="_blank" rel="noreferrer noopener">15 open source backup solutions to protect your data</a>
- <a href="http://allthingsopen.org/articles/10-common-linux-issues-how-to-fix" target="_blank" rel="noreferrer noopener">10 common Linux issues and the fast fixes you need</a>
- <a href="http://allthingsopen.org/articles/system76-meerkat-linux-developer-workstation" id="8422" type="articles" target="_blank" rel="noreferrer noopener">Meet the Meerkat: A compact Linux PC</a>
- <a href="http://allthingsopen.org/articles/6-best-linux-open-source-tutorials-2025" target="_blank" rel="noreferrer noopener">6 must-read Linux and open source tutorials</a>
- <a href="http://allthingsopen.org/articles/5-forces-driving-devops-ai-2026" target="_blank" rel="noreferrer noopener">5 forces driving DevOps and AI in 2026</a>

</div>

---

<div class="cc-license">

<a href="https://creativecommons.org/licenses/by-sa/4.0/" rel="license"><img src="https://allthingsopen.org/wp-content/themes/ato-main-2024/img/cc/by-sa.png" title="This work is licensed under a Creative Commons Attribution-Share Alike 4.0 International License." alt="Creative Commons License" /></a>

This work is licensed under a Creative Commons Attribution-Share Alike 4.0 International License.

