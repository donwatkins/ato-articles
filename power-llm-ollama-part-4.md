# Harness the power of large language models part 4: Working with an AI chef

Learn how to use the Llama3.1 model to create a custom model for cooking.

**By Don Watkins**  
**Published:** October 15, 2024  
**Source:** [https://allthingsopen.org/articles/power-llm-ollama-part-4](https://allthingsopen.org/articles/power-llm-ollama-part-4)

<figure class="featured">
<img src="https://allthingsopen.org/wp-content/uploads/2024/09/ollama_part-04.jpg" class="featured" alt="Silhouette of a llama in the desert - Part 4" />
<figcaption>Image by <a href="https://pixabay.com/users/sebadelval-18044/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=74770">sebastian del val</a> from <a href="https://pixabay.com//?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=74770">Pixabay</a></figcaption>
</figure>

Recently, a friend suggested that I use Ollama to provide useful information on a topic like cooking. I used my experiences customizing a model file and the latest iteration of <a href="https://ollama.com/library/llama3.1" target="_blank" rel="noreferrer noopener">Llama3.1</a> to accomplish that goal. I would assume that you already have Ollama installed on your computer, if not, read part one of the series, *<a href="http://allthingsopen.org/articles/power-llm-ollama-part-1" target="_blank" rel="noreferrer noopener">Getting started with Ollama</a>* for details on how to download and install `ollama`.

Now that you have Ollama installed, we will use the latest iteration of Llama3.1 and download the model to my computer.

``` wp-block-prismatic-blocks
ollama pull llama3.1
```

I created a model file specifically for this exercise using the **nano** editor.

``` wp-block-prismatic-blocks
  GNU nano 7.2                         cooking                                  
FROM llama3.1:latest

# set the temperature to 1 (higher is more creative, lower is more coherent
PARAMETER temperature 1

# Set the system prompt
SYSTEM """

You are a master chef. You provide detailed gluten free recipes on request.
"""
```

Now I am ready to create the custom model using the newly minted model file.

``` wp-block-prismatic-blocks
$ ollama create cooking -f ./cooking
```

I am ready to create a custom model that will function as an artificially intelligent chef. I run the model with the following command:

``` wp-block-prismatic-blocks
$ ollama run cooking
```

**Read more: <a href="http://allthingsopen.org/articles/getting-started-llamafile-tutorial" target="_blank" rel="noreferrer noopener">Getting started with Llamafile tutorial</a>**

I gave my intelligent assistant the following prompt:

``` wp-block-prismatic-blocks
>>>you have peanut butter, milk and honey provide one good gluten free meal recipe.

What a delightful combination! Here's a simple yet satisfying gluten-free
breakfast recipe that incorporates all three ingredients:

Gluten-Free Peanut Butter Pancakes with Honey and Milk

Servings: 4-6 people

Ingredients:

1 cup peanut butter (make sure it's free from cross-contamination with
gluten)
1/2 cup milk (you can use any type of milk, such as almond, coconut, or
dairy-based)
1 large egg
1 teaspoon vanilla extract
Pinch of salt
Honey for serving (about 2-3 tablespoons per person)
Instructions:

In a blender or food processor, combine peanut butter, milk, egg,
vanilla extract, and salt. Blend until smooth.
The batter should be thick but still pourable. If it's too thick, you
can add a little more milk. If it's too thin, you can add a bit more
peanut butter.
Heat a non-stick skillet or griddle over medium heat. Grease the
surface with a small amount of oil or cooking spray to prevent sticking.
Using a 1/4 cup measuring cup, scoop the batter onto the skillet or
griddle.
Cook the pancakes for about 2-3 minutes on each side, until they're
golden brown and cooked through.
Serve the peanut butter pancakes hot with a drizzle of honey. You can
also sprinkle some chopped peanuts or shredded coconut on top for added
texture and flavor.
Tips and Variations:

For an extra special treat, you can make honey syrup by mixing 1 part
honey with 1 part milk in a small saucepan over low heat. Whisk until the
mixture is smooth and warm.
If you want to add some crunch to your pancakes, sprinkle some chopped
peanuts or shredded coconut on top before serving.
Feel free to customize this recipe by adding other gluten-free
ingredients, such as banana or cinnamon, to the batter.
```

Enjoy your delicious gluten-free peanut butter pancakes with honey! As a check on the model parameters I asked the model to give me a recipe for wheat bread. It responded with the following caveat.

``` wp-block-prismatic-blocks
"I'd be happy to provide you with a traditional wheat bread recipe!

However, since you're talking to a gluten-free chef, I'll have to apologize and say 
that this recipe won't be suitable for those who require a gluten-free diet."
```

## More from We Love Open Source

- Read part one of this tutorial series: <a href="http://allthingsopen.org/articles/power-llm-ollama-part-1" target="_blank" rel="noreferrer noopener">Getting started with Ollama</a>
- Read part two of this tutorial series: <a href="http://allthingsopen.org/articles/power-llm-ollama-part-2" target="_blank" rel="noreferrer noopener">Working with Ollama</a>
- Read part two of this tutorial series: <a href="http://allthingsopen.org/articles/power-llm-ollama-part-3" target="_blank" rel="noreferrer noopener">Create your own model with Ollama</a>
- <a href="http://allthingsopen.org/articles/extend-local-ai-co-pilot-framework" target="_blank" rel="noreferrer noopener">4 ways to extend your local AI co-pilot framework</a>
- <a href="http://allthingsopen.org/articles/building-a-rag-system-with-googles-gemma-hugging-face-and-mongodb" target="_blank" rel="noreferrer noopener">Building a RAG system with Google’s Gemma, Hugging Face, and MongoDB</a>

------------------------------------------------------------------------

This article is adapted from “*<a href="https://donwatkins.info/2024/09/16/working-with-my-ai-chef/" target="_blank" rel="noreferrer noopener">Working with my AI chef</a>*” by Don Watkins, and is republished with permission from the author.

</div>

---

<div class="cc-license">

<a href="https://creativecommons.org/licenses/by-sa/4.0/" rel="license"><img src="https://allthingsopen.org/wp-content/themes/ato-main-2024/img/cc/by-sa.png" title="This work is licensed under a Creative Commons Attribution-Share Alike 4.0 International License." alt="Creative Commons License" /></a>

This work is licensed under a Creative Commons Attribution-Share Alike 4.0 International License.

