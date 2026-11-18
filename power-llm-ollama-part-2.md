# Harness the power of large language models part 2: Working with Ollama

Go in-depth with Ollama and open source AI on your local system.

**By Don Watkins**  
**Published:** October 1, 2024  
**Source:** [https://allthingsopen.org/articles/power-llm-ollama-part-2](https://allthingsopen.org/articles/power-llm-ollama-part-2)

<figure class="featured">
<img src="https://allthingsopen.org/wp-content/uploads/2024/09/ollama_part-02.jpg" class="featured" alt="Silhouette of a llama in the desert - Part 2" />
<figcaption>Image by <a href="https://pixabay.com/users/sebadelval-18044/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=74770">sebastian del val</a> from <a href="https://pixabay.com//?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=74770">Pixabay</a></figcaption>
</figure>

Now that I’m working with Ollama, I needed to figure out how to locate the models on my storage medium and determine the amount of space they were occupying. This is especially important for the MacBook Air, which has a 256 GB drive that is already half full. My Linux computer, on the other hand, has a terabyte NVME drive, so I’m not as worried about storage there. However, I still like to track where everything is and how much storage it uses. I wanted to compile a list of the downloaded models and learn how to delete them.

After Ollama is installed you can get a list of the commands available to you by entering the following command in the terminal.

``` wp-block-prismatic-blocks
$ ollama help

Usage:
ollama [flags]
ollama [command]

Available Commands:
serve Start ollama
create Create a model from a Modelfile
show Show information for a model
run Run a model
pull Pull a model from a registry
push Push a model to a registry
list List models
ps List running models
cp Copy a model
rm Remove a model
help Help about any command

Flags:
-h, --help help for ollama
-v, --version Show version information
```

Check the version of `ollama` you are using with:

``` wp-block-prismatic-blocks
$ ollama -v

ollama version is 0.3.9
```

Downloading models is easy using `ollama pull`:  
  
`$ ollama pull gemma2`

This downloads the `gemma2` large language model to your local computer. You can also initiate a pull request by running the following command:

``` wp-block-prismatic-blocks
$ ollama run phi3
```

**Read more: <a href="http://allthingsopen.org/articles/getting-started-llamafile-tutorial" target="_blank" rel="noreferrer noopener">Getting started with Llamafile tutorial</a>**

This command sequence pulls the `phi3` model down to your computer. After I had tried a few models I wanted to get a sense of how much space they were taking on my system and I used the `list` or `ls` switch of the `ollama` command.

``` wp-block-prismatic-blocks
$ ollama list
NAME                ID              SIZE    MODIFIED     
llama3.1:latest     f66fc8dc39ea    4.7 GB  2 hours ago     
codegemma:latest    0c96700aaada    5.0 GB  43 hours ago    
phi3:latest         4f2222927938    2.2 GB  47 hours ago    
gemma2:latest       ff02c3702f32    5.4 GB  3 days ago      
phi3:medium         cf611a26b048    7.9 GB  3 days ago      
gemma2:2b           8ccf136fdd52    1.6 GB  3 days ago  
```

Now I can see how much storage the models are using. It’s easy to delete a model. I decided to delete the oldest one first.

``` wp-block-prismatic-blocks
$ ollama rm gemma2
deleted 'gemma2'
```

Just to be sure, I ran `ollama ls`; sure enough, the model was gone.

``` wp-block-prismatic-blocks
NAME             ID              SIZE    MODIFIED     
llama3.1:latest     f66fc8dc39ea    4.7 GB  2 hours ago     
codegemma:latest    0c96700aaada    5.0 GB  44 hours ago    
phi3:latest         4f2222927938    2.2 GB  47 hours ago    
phi3:medium 
```

You can check on how many models are running on your machine with the following command:

``` wp-block-prismatic-blocks
$ ollama ps
NAME        ID              SIZE    PROCESSOR   UNTIL              
phi3:latest 4f2222927938    6.0 GB  100% CPU    4 minutes from now
```

Using the `show` command shows you information about the model.

``` wp-block-prismatic-blocks
ollama show phi3
  Model                                 
    arch                phi3                    
    parameters          3.8B                    
    quantization        Q4_0                    
    context length      131072                  
    embedding length    3072                    
                                          
  Parameters                            
    stop    "<|end|>"                            
    stop    "<|user|>"                           
    stop    "<|assistant|>"                      
                                          
  License                               
    Microsoft.                                
    Copyright (c) Microsoft Corporation.
```

Stop a model from running by pressing `CTRL +c`. Exit the model by entering `CTRL +d`.

In conclusion, Ollama has revolutionized our understanding and interaction with AI. With this tutorial, you can now track where everything is and how much storage the LLMs you’ve downloaded are using on your system.

## More from We Love Open Source

- Read part one of this tutorial series: <a href="http://allthingsopen.org/articles/power-llm-ollama-part-1" target="_blank" rel="noreferrer noopener">Getting started with Ollama</a>
- <a href="http://allthingsopen.org/articles/power-llm-ollama-part-1" target="_blank" rel="noreferrer noopener">Harness the power of large language models part 1: Getting started with Ollama</a>
- <a href="http://allthingsopen.org/articles/open-source-by-pieces-ai-dev-tool" target="_blank" rel="noreferrer noopener">Open Source by Pieces: A community for AI-enabled dev tool enthusiasts</a>
- <a href="http://allthingsopen.org/articles/building-a-rag-system-with-googles-gemma-hugging-face-and-mongodb" target="_blank" rel="noreferrer noopener">Building a RAG system with Google’s Gemma, Hugging Face, and MongoDB</a>

This article is adapted from “<a href="https://donwatkins.info/2024/09/09/working-with-ollama/" target="_blank" rel="noreferrer noopener"><em>Working with Ollama</em></a>” by Don Watkins, and is republished with permission from the author.

</div>

---

<div class="cc-license">

<a href="https://creativecommons.org/licenses/by-sa/4.0/" rel="license"><img src="https://allthingsopen.org/wp-content/themes/ato-main-2024/img/cc/by-sa.png" title="This work is licensed under a Creative Commons Attribution-Share Alike 4.0 International License." alt="Creative Commons License" /></a>

This work is licensed under a Creative Commons Attribution-Share Alike 4.0 International License.

