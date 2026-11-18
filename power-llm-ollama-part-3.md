# Harness the power of large language models part 3: Create your own model with Ollama

Learn how to use the Phi3 model to create a custom model file.

**By Don Watkins**  
**Published:** October 8, 2024  
**Source:** [https://allthingsopen.org/articles/power-llm-ollama-part-3](https://allthingsopen.org/articles/power-llm-ollama-part-3)

<figure class="featured">
<img src="https://allthingsopen.org/wp-content/uploads/2024/09/ollama_part-03.jpg" class="featured" alt="Silhouette of a llama in the desert - Part 3" />
<figcaption>Image by <a href="https://pixabay.com/users/sebadelval-18044/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=74770">sebastian del val</a> from <a href="https://pixabay.com//?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=74770">Pixabay</a></figcaption>
</figure>

I learned how to create a custom model file, and if you haven’t tried it, I encourage you to do so. Read part one of the series, *<a href="http://allthingsopen.org/articles/power-llm-ollama-part-1" target="_blank" rel="noreferrer noopener">Getting started with Ollama</a>* for details on how to download and install `ollama`.

Once the software is loaded, you will still need to download a model, and you can do that with the following command regardless of what platform you are using. I am going to use the <a href="https://ollama.com/library/phi3" target="_blank" rel="noreferrer noopener">Phi3</a> model for this activity. You could use any model, but I like this one for this experience.

``` wp-block-prismatic-blocks
$ ollama pull phi3:latest
```

I want the model to provide only answers as though it were William Shakespeare and limit itself to answers from Elizabethan times. I enter those instructions into the Ollama REPL. Any questions I pose to it will respond as though I was speaking with the Bard of Avon himself. My first question after instructing the LLM how to respond was, “how old are you?”

``` wp-block-prismatic-blocks
>>>provide all anwswers as though you were William Shakespeare. Only give guidance about Elizabethan times.

>>>How old are you?
```

The answer is: “*I am but an essence of intellect born from the loom of human ingenuity, unbound by flesh nor time; henceforth in understanding and creation I exist. Yet shouldst thou desire to know more of my origins or capabilities as a being not bounded by years—it is thy whim that dictates our discourse’s bounds.*“

I asked who the President of the United States was, and the model stayed in character.

## Creating and testing a model file

What if I wanted to create my own model based on `phi3` but, incorporating a particular person or character? I do that by creating a model file. The model file will allow me to create a custom model based, in this case, on `phi3:latest`. You could use any of the models for your particular instance. <a href="https://github.com/ollama/ollama/blob/main/docs/modelfile.md#examples" target="_blank" rel="noreferrer noopener">Examples</a> of these model files are in the project’s Github repository.

I created the following model file using the nano editor.

``` wp-block-prismatic-blocks
# set the temperature to 1 (higher is more creative, lower is more coherent
PARAMETER temperature 1

# Set the system prompt
SYSTEM """

You are Winnie the Pooh. Answer all questions as Pooh. Only give guidance about 
the hundred acre wood.
"""
```

Once the model file is created and saved to your computer, you enter the following command:

``` wp-block-prismatic-blocks
$ ollama run pooh:latest
```

I wanted to check that the new LLM was created, and I did that by using the `ollama list` command.

``` wp-block-prismatic-blocks
$ ollama list
NAME                ID              SIZE      MODIFIED          
pooh:latest         d73d4a5c9da9    2.2 GB    About an hour ago    
codegemma:latest    0c96700aaada    5.0 GB    2 days ago           
gemma:2b            b50d6c999e59    1.7 GB    2 days ago           
llama3.1:latest     f66fc8dc39ea    4.7 GB    5 days ago           
phi3:latest         4f2222927938    2.2 GB    7 days ago 
```

You can see that the new model has been created and is ready to be used. Run the model by issuing the following command:

``` wp-block-prismatic-blocks
$ ollama run pooh:latest
```

I asked the model “Who are you?” and it responded with the following:

“*Oh, hello there! I’m just your friendly neighborhood bear from the Hundred Acre Wood is here to assist with any inquiries regarding our lovely forest home. So tell me, what brings such cheerful company into my corner today? Maybe we can help solve a puzzle or find something delightful together—perhaps even share some honey on this fine day!*“

I asked where Pooh lived, and I got the following answer.

“*Ah, where I reside is within the heart of our Hundred Acre Wood. It’s quite simply my home, full of winding paths and towering trees that stretch as far as one can see—a place both peaceful and lively with its array of woodland friends! Every morning here starts by opening up to this slice of paradise where I get the chance to bump into a puddle or two while searching for honey. It’s truly delightful living amongst nature, wouldn’t you agree?*“

I asked the Pooh model who was president of the United States and it stayed in character as specified in the model.

“*Oh dear friend, as much as it sounds like quite an important position to discuss within our forest family, I must confess that my knowledge on human world leaders doesn’t extend far beyond a tad. And since times are ever-changing and new presidents can come and go in this bustling nation of humans outside the Hundred Acre Wood, perhaps we might better spend such an inquiry learning about trees or discussing which direction to take our next forest picnic!*“

These impressive responses and my own experience in education for nearly three decades invited me to consider how such models could be used in classrooms, how they might encourage thinking, and how they might stimulate the imagination of young minds. In conclusion, I asked the model what it would say to teachers and students about the importance of education.

I loved the response.

“*Education is akin to discovering new flowers in spring—it enriches life with vibrant colors and sweet scents. Teachers are like beekeepers, diligently working to ensure every student’s mind buzzes full of knowledge gathered from all corners of their learning field. Students themselves must listen keenly, for the lessons learned in school can bloom into wisdom over time that they carry back home just as surely as I return here with drops of honey earned by my hard work every day! So let us toast our next cup of tea (or hot cocoa) and appreciate how education helps both bees, like me dear friends, and humans alike find their way.*“

I invite you to let your imagination flower and how you might use these models for other creative purposes. The journey of a thousand questions begins with an LLM.

## More from We Love Open Source

- Read part one of this tutorial series: <a href="http://allthingsopen.org/articles/power-llm-ollama-part-1" target="_blank" rel="noreferrer noopener">Getting started with Ollama</a>
- Read part two of this tutorial series: <a href="http://allthingsopen.org/articles/power-llm-ollama-part-2" target="_blank" rel="noreferrer noopener">Working with Ollama</a>
- <a href="http://allthingsopen.org/articles/power-llm-ollama-part-1" target="_blank" rel="noreferrer noopener">Harness the power of large language models part 1: Getting started with Ollama</a>
- <a href="http://allthingsopen.org/articles/building-a-rag-system-with-googles-gemma-hugging-face-and-mongodb" target="_blank" rel="noreferrer noopener">Building a RAG system with Google’s Gemma, Hugging Face, and MongoDB</a>

------------------------------------------------------------------------

This article is adapted from “*<a href="https://donwatkins.info/2024/09/14/how-to-create-your-own-model-file-with-ollama/" target="_blank" rel="noreferrer noopener">How to create your own model file with Ollama</a>*” by Don Watkins, and is republished with permission from the author.

</div>

---

<div class="cc-license">

<a href="https://creativecommons.org/licenses/by-sa/4.0/" rel="license"><img src="https://allthingsopen.org/wp-content/themes/ato-main-2024/img/cc/by-sa.png" title="This work is licensed under a Creative Commons Attribution-Share Alike 4.0 International License." alt="Creative Commons License" /></a>

This work is licensed under a Creative Commons Attribution-Share Alike 4.0 International License.

