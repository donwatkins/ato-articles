# How to run local LLMs in a container with Ollama and Podman

A step-by-step Podman tutorial with CPU and NVIDIA GPU options, from your first volume to your first prompt.

**By Don Watkins**  
**Published:** October 28, 2026  
**Source:** [https://allthingsopen.org/articles/run-local-llms-container-ollama-podman](https://allthingsopen.org/articles/run-local-llms-container-ollama-podman)

<figure class="featured">
<img src="https://allthingsopen.org/wp-content/uploads/2026/10/llama-warning-sign-e1791947247380.jpg" class="featured" alt="llama crossing warning sign next to a road" />
<figcaption>Image by <a href="https://pixabay.com/users/dassel-989431/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=2677398">Aline Dassel</a> from <a href="https://pixabay.com//?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=2677398">Pixabay</a></figcaption>
</figure>

Containers aren’t new, but I am new to using them. I’m particularly interested in locally hosted AI, and I’ve written several articles about using Ollama, GenAI, and other locally installed large language models (LLMs) on my Linux desktop. In this article, I’ll share my experience setting up Ollama in a container. Running Ollama in a container simplifies dependency management, prevents conflicts on your workstation, and helps keep your development environment consistent.

An old friend began experimenting with locally hosted AI, and since I’d been working with containers, I thought, why not give Ollama another try in a container environment? I found a good how-to from <a href="https://fedoramagazine.org/running-ollama-locally-with-podman-on-fedora-linux/" target="_blank" rel="noreferrer noopener">Fedora Magazine</a> and adapted it for my own use.

## Install Podman on Linux

First, you will need to install Podman. I used Flatpak for my installation, but you can use `dnf` on Fedora or `apt` on Ubuntu and Debian.

``` wp-block-prismatic-blocks
sudo dnf -y install podman
```

``` wp-block-prismatic-blocks
sudo apt-get -y install podman
```

## Create a persistent volume for Ollama models

Once Podman is installed, open a terminal and enter the following:

``` wp-block-prismatic-blocks
podman volume create ollama_storage
```

This creates a storage volume for the models you download. Because LLM weights are large, a persistent volume ensures they aren’t lost when the container stops.

## Run Ollama in a Podman container

Now you’re ready to run the Ollama container. Enter the following command in a terminal:

``` wp-block-prismatic-blocks
podman run -d \
  --name ollama \
  -v ollama_storage:/root/.ollama \
  -p 11434:11434 \
  docker.io/ollama/ollama:latest
```

I couldn’t run a container on my setup using the specified ports, so I changed the port setting to 4134, and the container ran flawlessly.

## Run Ollama with NVIDIA GPU support

I don’t have an NVIDIA GPU, which would be ideal for this setup, so the command above is for CPU-only installations. If you do have one, run this command instead:

``` wp-block-prismatic-blocks
podman run -d \
  --name ollama \
  --security-opt=label=disable \
  --device nvidia.com/gpu=all \
  -v ollama_storage:/root/.ollama \
  -p 11434:11434 \
  docker.io/ollama/ollama:latest
```

## Check that the Ollama container is running

Now open Podman and make sure your newly created container is running.

<div class="wp-block-image">

<figure class="aligncenter size-full">
<img src="https://allthingsopen.org/wp-content/uploads/2026/10/open-podman.png" class="wp-image-9596" data-fetchpriority="high" decoding="async" srcset="https://allthingsopen.org/wp-content/uploads/2026/10/open-podman.png 517w, https://allthingsopen.org/wp-content/uploads/2026/10/open-podman-300x67.png 300w" sizes="(max-width: 517px) 100vw, 517px" width="517" height="115" alt="Podman console showing llama-stack and ollama is running" />
<figcaption>Screen capture by Don Watkins CC by SA 4.0</figcaption>
</figure>

</div>

## Pull and run your first model with Llama 3

With the container running, you’re ready to pull down your first model and start experimenting with your locally hosted LLM. Do that by entering the following command:

``` wp-block-prismatic-blocks
podman exec -it ollama ollama run llama3
```

Depending on your internet speed, this might take a few minutes, and then you’ll be ready to use the Llama 3 model in Ollama. At the prompt, I asked the model for a simple fact about Linux Mint. This was the result:

``` wp-block-prismatic-blocks
>>> tell me a fun fact about Linux Mint
Here's a fun fact:

Linux Mint is a Linux distribution that was created by Clement Lefebvre, a 
French programmer, in 2006. What's interesting is that Linux Mint was 
originally intended to be a Ubuntu-based distribution, but it quickly 
gained popularity and became a standalone project in 2009. Today, Linux 
Mint is one of the most popular Linux distributions in the world, with 
over 3 million users!
```

## Why run Ollama in a container?

Setting up Ollama in a container provides a streamlined way to experiment with locally hosted AI models while managing dependencies and avoiding conflicts. With Podman and a few configuration tweaks, you can create a consistent, isolated setup for running models on your own machine.

## More from We Love Open Source

- <a href="http://allthingsopen.org/articles/15-open-source-backup-solutions-2026" target="_blank" rel="noopener">15 open source backup solutions to protect your data</a>
- <a href="https://allthingsopen.org/articles/5-common-mistakes-new-linux-users" target="_blank" rel="noopener">The 5 most common mistakes new Linux users make</a>
- <a href="https://allthingsopen.org/articles/5-linux-tools-clear-cache-remove-packages-manage-logs" target="_blank" rel="noopener">An open source alternative to AirDrop for Linux and Mac users</a>
- <a href="https://allthingsopen.org/articles/5-linux-tools-clear-cache-remove-packages-manage-logs" target="_blank" rel="noopener">5 Linux tools to clear cache, remove old packages, and manage logs</a>
- <a href="https://allthingsopen.org/articles/why-my-podman-install-failed-on-macos" target="_blank" rel="noopener">Why my Podman install failed on macOS</a>

This article is adapted from “<a href="https://donwatkins.info/2026/10/03/running-ollama-in-a-container-a-beginners-guide/" target="_blank" rel="noopener"><em>Running Ollama in a container: A beginner’s guide</em></a>” by Don Watkins, and is republished with permission from the author.

</div>

---

<div class="cc-license">

<a href="https://creativecommons.org/licenses/by-sa/4.0/" rel="license"><img src="https://allthingsopen.org/wp-content/themes/ato-main-2024/img/cc/by-sa.png" title="This work is licensed under a Creative Commons Attribution-Share Alike 4.0 International License." alt="Creative Commons License" /></a>

This work is licensed under a Creative Commons Attribution-Share Alike 4.0 International License.

