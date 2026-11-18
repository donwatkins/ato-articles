# A quick guide to create an efficient rubric using genAI

A developer's tutorial for writing effective rubrics with Ollama

**By Don Watkins**  
**Published:** October 10, 2024  
**Source:** [https://allthingsopen.org/articles/rubric-guide-using-genai](https://allthingsopen.org/articles/rubric-guide-using-genai)

<figure class="featured">
<img src="https://allthingsopen.org/wp-content/uploads/2024/07/track-and-field-1867053_1920-e1720494533421.jpg" class="featured" alt="Track and field lanes 2 through 6." />
<figcaption>Image by <a href="https://pixabay.com/users/pexels-2286921/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=1867053">Pexels</a> from <a href="https://pixabay.com//?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=1867053">Pixabay</a></figcaption>
</figure>

In my previous article, I discussed using Ollama and the Llama3.1 model to assess my writing. Since I’m new to teaching writing, I was curious to see if Ollama could generate an evaluation rubric for grading student writing and then use that rubric to evaluate a sample of student writing.

I am going to assume that you have already installed Ollama on your computer and downloaded the Llama3.1 model. If not, be sure to follow the directions provided in the previous article.

Start Ollama and run the model:

``` wp-block-prismatic-blocks
$ ollama run llama3.1:latest

>>>Develop a assesment rubric for the evaluation of undergraduate student writing
```

Here is the assessment rubric that was created by Ollama and Llama3.1:

<div class="wp-block-group">

<div class="wp-block-group__inner-container is-layout-constrained wp-block-group-is-layout-constrained">

<div class="wp-block-group has-cyan-bluish-gray-background-color has-background">

<div class="wp-block-group__inner-container is-layout-constrained wp-block-group-is-layout-constrained">

**Content (40 points)**

- **Thesis Statement**: Does the thesis statement clearly and concisely present the main argument or claim? (5 points)
  - 4: The thesis statement is clear, concise, and well-supported by evide evidence.
  - 3: The thesis statement is mostly clear and concise, but may lack some supporting evidence.
  - 2: The thesis statement is somewhat unclear or lacking in concision, but has some supporting evidence.
  - 1: The thesis statement is unclear, vague, or lacks supporting evidence.
- **Argumentation**: Are the arguments presented well-supported by evidence? (10 points)
  - 9-10: Strong arguments are presented with ample and relevant evidence to support them.
  - 7-8: Good arguments are presented, but may lack some relevant evidence.
  - 5-6: Fair arguments are presented, but may be lacking in supporting ev evidence.
  - 0-4: Poor or absent argumentation.
- **Analysis**: Is the analysis of the topic thorough and insightful? (10 points)
  - 9-10: The analysis is thorough, well-supported, and offers new insights into the topic.
  - 7-8: Good analysis is presented, but may lack some depth or insight.
  - 5-6: Fair analysis is presented, but may be lacking in detail or insig insight.
  - 0-4: Poor or absent analysis.
- **Counterarguments**: Are counterarguments addressed and refuted effectively? (5 points)
  - 4: Effective counterarguments are presented and refuted with strong ev evidence.
  - 3: Some counterarguments are acknowledged, but not fully refuted.
  - 2: Few counterarguments are mentioned or refuted poorly.
  - 1: No counterarguments are addressed.

**Organization (20 points)**

- **Introduction**: Is the introduction engaging and effective in setting up the rest of the paper? (5 points)
  - 4: The introduction is clear, concise, and effectively sets up the rest of the paper.
  - 3: The introduction is mostly clear and concise, but may lack some eng engagement or clarity.
  - 2: The introduction is somewhat unclear or lacking in concision.
  - 1: The introduction is weak or absent.
- **Body Paragraphs**: Are the body paragraphs well-organized and logically connected? (10 points)
  - 9-10: Strong organization and logical connections between paragraphs are evident.
  - 7-8: Good organization and some logical connections, but may be lacking in coherence.
  - 5-6: Fair organization and some attempts at connecting paragraphs.
  - 0-4: Poor or absent organization.
- **Conclusion**: Is the conclusion effective in summarizing the main points and reiterating the thesis? (5 points)
  - 4: The conclusion is clear, concise, and effectively summarizes the main points.
  - 3: The conclusion is mostly clear and concise, but may lack some summary or repetition of the thesis.
  - 2: The conclusion is somewhat unclear or lacking in concision.
  - 1: The conclusion is weak or absent.

**Style (20 points)**

- **Writing Style**: Is the writing style clear, concise, and engaging? (10 points)
  - 9-10: Strong writing style is evident, with clear, concise language and engaging tone.
  - 7-8: Good writing style is present, but may lack some clarity or conci concision.
  - 5-6: Fair writing style is present, but may be lacking in clarity or e engagement.
  - 0-4: Poor or absent writing style.
- **Mechanics**: Are grammar, spelling, and punctuation accurate? (5 points)
  - 4: Strong attention to detail and accuracy in mechanics.
  - 3: Good attention to detail and some accuracy, but may be lacking in others.
  - 2: Fair attention to detail, with some errors in mechanics.
  - 1: Poor or absent attention to detail.

**Mechanics (20 points)**

- **Grammar**: Is grammar accurate and effective? (5 points)
  - 4: Strong grammar is present throughout the paper.
  - 3: Good grammar is mostly present, but may be lacking in some areas.
  - 2: Fair grammar is present, with some errors.
  - 1: Poor or absent grammar.
- **Spelling**: Is spelling accurate and effective? (5 points)
  - 4: Strong spelling is evident throughout the paper.
  - 3: Good spelling is mostly present, but may be lacking in some areas.
  - 2: Fair spelling is present, with some errors.
  - 1: Poor or absent spelling.
- **Punctuation**: Is punctuation accurate and effective? (5 points)
  - 4: Strong punctuation is evident throughout the paper.
  - 3: Good punctuation is mostly present, but may be lacking in some areas.
  - 2: Fair punctuation is present, with some errors.
  - 1: Poor or absent punctuation.

**Total**: The total score will range from 0 to 100 points.

</div>

</div>

</div>

</div>

**Read more: <a href="http://allthingsopen.org/articles/enhance-writing-skills-ollama-phi3" target="_blank" rel="noreferrer noopener">Enhance your writing skills with Ollama and Phi3</a>**

I copied and pasted the text from the article I wrote in 2022 about [12 Essential Linux Commands for Beginners](https://opensource.com/article/22/5/essential-linux-commands) and asked Ollama to evaluate that article using the rubric it had just created. Here is the result:

<div class="wp-block-group">

<div class="wp-block-group__inner-container is-layout-constrained wp-block-group-is-layout-constrained">

<div class="wp-block-group has-cyan-bluish-gray-background-color has-background">

<div class="wp-block-group__inner-container is-layout-constrained wp-block-group-is-layout-constrained">

**Content**

- The article provides a comprehensive list of 12 essential Linux commands, along with explanations, examples, and usage tips.
- The topics covered are relevant to both beginners and experienced users.
- The tone is conversational and easy to understand.

**Organization**

- The article is well-structured, with each command introduced as a separate section.
- The sections are concise and to the point, making it easy for readers to quickly grasp the key concepts.
- The use of headings and subheadings helps to break up the content and make it more readable.

**Writing Style**

- The writing style is clear, concise, and engaging.
- The author uses everyday language, avoiding technical jargon whenever possible.
- The text includes humorous anecdotes and personal experiences, making it more relatable and entertaining.

**Structure and Pacing**

- The article flows smoothly from one command to the next, with each section building on the previous one.
- The pacing is well-balanced, with sufficient information provided for readers to understand the concepts without feeling overwhelmed.
- The use of examples and exercises helps to reinforce learning and keep readers engaged.

**Technical Quality**

- The technical accuracy of the article appears to be high, with correct usage examples and syntax.
- The author provides sufficient context and explanations for each command, making it easy for readers to understand their functionality.
- The inclusion of links to external resources (e.g., `trashy` and `trash-cli`) adds value and helps readers explore further.

**Originality and Depth**

- While the article covers familiar topics, it offers a fresh perspective and new insights into each command.
- The author provides additional context and explanations that go beyond mere listing of commands.
- The inclusion of personal anecdotes and experiences adds depth and relatability to the content.

**Conclusion and Future Work**

- The article concludes with an open-ended question, encouraging readers to share their favorite Linux commands.
- This approach fosters engagement and encourages further discussion, which can be beneficial for building a community around Linux and its usage.

Overall, I would give this article a score of 4.5 out of 5 in content, organization, writing style, structure and pacing, technical quality, originality and depth, and conclusion and future work. The only area where it could improve is by providing more advanced or specialized topics for experienced users.

</div>

</div>

</div>

</div>

Incorporating Ollama into your rubric development process cannot only streamline the creation of evaluation criteria but, also enhances the overall quality of assessments. By harnessing the power of genAI, educators can save time, reduce ambiguity, and focus on what truly matters, like supporting student learning and growth.

## More from We Love Open Source

- <a href="http://allthingsopen.org/articles/enhance-writing-skills-ollama-phi3" target="_blank" rel="noreferrer noopener">Enhance your writing skills with Ollama and Phi3</a>
- <a href="http://allthingsopen.org/articles/getting-started-llamafile-tutorial" target="_blank" rel="noreferrer noopener">Getting started with Llamafile tutorial</a>
- <a href="http://allthingsopen.org/articles/extend-local-ai-co-pilot-framework" target="_blank" rel="noreferrer noopener">4 ways to extend your local AI co-pilot framework</a>
- <a href="http://allthingsopen.org/articles/power-llm-ollama-part-1" target="_blank" rel="noreferrer noopener">Harness the power of large language models part 1: Getting started with Ollama</a>

This article is adapted from “<a href="https://donwatkins.info/2024/09/23/using-ollama-to-write-an-evaluation-rubric/" target="_blank" rel="noreferrer noopener">Using Ollama to write an evaluation rubric</a>” by Don Watkins, and is republished with permission from the author.

</div>

---

<div class="cc-license">

<a href="https://creativecommons.org/licenses/by-sa/4.0/" rel="license"><img src="https://allthingsopen.org/wp-content/themes/ato-main-2024/img/cc/by-sa.png" title="This work is licensed under a Creative Commons Attribution-Share Alike 4.0 International License." alt="Creative Commons License" /></a>

This work is licensed under a Creative Commons Attribution-Share Alike 4.0 International License.

