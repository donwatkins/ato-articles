# Harness the power of large language models part 1: Getting started with Ollama

Explore using Ollama and open source AI on your local system.

**By Don Watkins**  
**Published:** September 25, 2024  
**Source:** [https://allthingsopen.org/articles/power-llm-ollama-part-1](https://allthingsopen.org/articles/power-llm-ollama-part-1)

<figure class="featured">
<img src="https://allthingsopen.org/wp-content/uploads/2024/09/ollama_part-01.jpg" class="featured" alt="Silhouette of a llama in the desert - Part 1" />
<figcaption>Image by <a href="https://pixabay.com/users/sebadelval-18044/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=74770">sebastian del val</a> from <a href="https://pixabay.com//?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=74770">Pixabay</a></figcaption>
</figure>

Everywhere you look, someone is talking or writing about artificial intelligence. I have been keenly interested in the topic since my graduate school days in the 1990s. I have used ChatGPT, Microsoft Copilot, Claude, Stable Diffusion, and other AI software to experiment with how this technology works and satisfy my innate curiosity.

I discovered <a href="https://ollama.com/" target="_blank" rel="noreferrer noopener">Ollama</a>. Developed by Meta, it is an open source large language model (LLM) that can run locally on Linux, MacOS, and Microsoft Windows. There is a great deal of concern that while using LLMs in the cloud, your data is being scraped and reused by one of the major technology companies. Ollama is open source and has an MIT license. Since Ollama runs locally, there is no danger that your work could end up in someone else’s LLM.

The Ollama website proclaims, “Get up and running with Large Language Models.” That invitation was all I needed to get started. Open a terminal on Linux and enter the following to install Ollama:

``` wp-block-prismatic-blocks
curl -fsSL https://ollama.com/install.sh | sh
```

The project lists all the [models](https://ollama.com/library) that you can use, and I chose the first one in the list, Llama3.1. Installation is easy, and it did not take long to install the Llama3.1 model. I followed the instructions and, in the terminal, entered the following command:

``` wp-block-prismatic-blocks
$ ollama run llama3.1
```

The model began to install, which took a couple of minutes. This could vary depending on your CPU and internet connection. I have an Intel i7 with 64 GB RAM and a robust internet connection. Once the model was downloaded, I was prompted to ‘`talk`‘ with the LLM. I decided to ask a question about the history of my alma mater, St. Bonaventure University. I entered the following commands:

``` wp-block-prismatic-blocks
$ ollama run llama3.1
>>>What is the history of St. Bonaventure University?
```

The results were good but somewhat inaccurate. “*St. Bonaventure University is a private Franciscan university located in Olean, New York. The institution was founded by the Diocese of Buffalo and has a rich history dating back to 1856.*” St. Bonaventure is located near Olean, New York, and it is in the Diocese of Buffalo, but it was founded in 1858. I asked the model to name some famous St. Bonaventure alumni; more inaccuracies were comic. Bob Lanier was a famous alumnus but Danny Ainge was not.

**Read more: <a href="http://allthingsopen.org/articles/getting-started-llamafile-tutorial" target="_blank" rel="noreferrer noopener">Getting started with Llamafile tutorial</a>**

## Trying Ollama on different systems

The results are rendered in MarkDown, which is a real plus. I also knew that having a GPU would render the results much quicker. I wanted to install Ollama on my M2 MacBook Air which I soon did. I followed the much easier directions: Download the <a href="https://ollama.com/download/Ollama-darwin.zip" target="_blank" rel="noreferrer noopener">Ollama-darwin.zip</a>, unzip the archive, and double-click the Ollama icon. The program is installed in the MacBook’s Application folder. When the program is launched, it directs me to the Mac Terminal app, where I can enter the same commands I had entered on my Linux computer.

Unsurprisingly, Ollama uses a great deal of processing power, which is lessened if you run it on a computer with a GPU. My Intel NUC 11 is a very powerful desktop computer with quad-core 11th Gen Intel Core i7-1165G7, 64 gigabytes of RAM, and a robust connection to the internet to download additional models. I posed similar questions to the Llama3.1 model first on the Intel running Linux and then on the M2 MacBook Air running MacOS.

You can see the CPU utilization below on my Linux desktop. It’s pegged, and the output from the model is slow at an approximate rate of 50 words per minute. Contrast that with the M2 MacBook, which has a GPU with a CPU utilization of approximately 6.9% and words per minute faster than I could read.

<figure class="wp-block-image size-full">
<img src="http://allthingsopen.org/wp-content/uploads/2024/09/ollama_screenshot_01.png" class="wp-image-5648" data-fetchpriority="high" decoding="async" srcset="https://allthingsopen.org/wp-content/uploads/2024/09/ollama_screenshot_01.png 803w, https://allthingsopen.org/wp-content/uploads/2024/09/ollama_screenshot_01-300x105.png 300w, https://allthingsopen.org/wp-content/uploads/2024/09/ollama_screenshot_01-768x270.png 768w" sizes="(max-width: 803px) 100vw, 803px" width="803" height="282" alt="Ollama CPU screenhot" />
<figcaption>Image credits by Don Watkins CC BY SA 4.0</figcaption>
</figure>

## Creating Python code with Ollama

While Ollama Llama3.1 might not excel at history recall, it does very well when asked to create Python code. I entered a prompt to create Python code to create a circle without specifying how to accomplish the task. It rendered the code shown below. I had to install the `pygame` module, which is not on my system.

``` wp-block-prismatic-blocks
$  sudo apt install python3-pygame
# Python Game Development

import pygame
from pygame.locals import *

# Initialize the pygame modules
pygame.init()

# Create a 640x480 size screen surface
screen = pygame.display.set_mode((640, 480))

# Define some colors for easy reference
WHITE = (255, 255, 255)
RED = (255, 0, 0)

while True:
    # Handle events
    for event in pygame.event.get():
        if event.type == QUIT or (event.type == KEYDOWN and event.key == 
K_ESCAPE):
            pygame.quit()
            quit()

    screen.fill(WHITE)  # Fill the background with white color

    # Drawing a circle on the screen at position (250, 200), radius 100
    pygame.draw.circle(screen, RED, (250, 200), 100)
    
    # Update the full display Surface to the screen
    pygame.display.flip()
```

I copied the code into <a href="https://vscodium.com/" target="_blank" rel="noreferrer noopener">VSCodium</a> and ran it. You can see the results below.

<figure class="wp-block-image size-full">
<img src="http://allthingsopen.org/wp-content/uploads/2024/09/pygame.png" class="wp-image-5678" decoding="async" srcset="https://allthingsopen.org/wp-content/uploads/2024/09/pygame.png 635w, https://allthingsopen.org/wp-content/uploads/2024/09/pygame-300x238.png 300w" sizes="(max-width: 635px) 100vw, 635px" width="635" height="504" />
<figcaption>Image credits by Don Watkins CC BY SA 4.0</figcaption>
</figure>

As I continue experimenting with Ollama and other open source LLMs, I’m struck by the significance of this shift toward local, user-controlled AI. No longer are we forced to rely on cloud-based services that may collect our data without our knowledge or consent. With Ollama and similar projects, individuals can harness the power of language models while maintaining complete ownership over their work and personal information. This newfound autonomy is a crucial step forward for AI development and I’m eager to see where it takes us.

## More from We Love Open Source

- Read part two of this tutorial series: <a href="http://allthingsopen.org/articles/power-llm-ollama-part-2" target="_blank" rel="noreferrer noopener">Working with Ollama</a>
- <a href="http://allthingsopen.org/articles/extend-local-ai-co-pilot-framework" target="_blank" rel="noreferrer noopener">4 ways to extend your local AI co-pilot framework</a>
- <a href="http://allthingsopen.org/articles/building-a-rag-system-with-googles-gemma-hugging-face-and-mongodb" target="_blank" rel="noreferrer noopener">Building a RAG system with Google’s Gemma, Hugging Face, and MongoDB</a>

------------------------------------------------------------------------

This article is adapted from “*<a href="https://donwatkins.info/2024/09/07/breaking-free-from-the-cloud-exploring-the-benefits-of-localopen-source-ai-with-ollama/" target="_blank" rel="noreferrer noopener">Breaking Free from the Cloud: Exploring the Benefits of Local,Open-Source AI with Ollama</a>*” by Don Watkins, and is republished with permission from the author.

</div>

---

<div class="cc-license">

<a href="https://creativecommons.org/licenses/by-sa/4.0/" rel="license"><img src="https://allthingsopen.org/wp-content/themes/ato-main-2024/img/cc/by-sa.png" title="This work is licensed under a Creative Commons Attribution-Share Alike 4.0 International License." alt="Creative Commons License" /></a>

This work is licensed under a Creative Commons Attribution-Share Alike 4.0 International License.

