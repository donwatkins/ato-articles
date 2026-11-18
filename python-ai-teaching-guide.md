# Teaching Python with AI: A guide for educators

How to use AI as a teaching partner that encourages critical thinking instead of code copying.

**By Don Watkins**  
**Published:** July 29, 2026  
**Source:** [https://allthingsopen.org/articles/python-ai-teaching-guide](https://allthingsopen.org/articles/python-ai-teaching-guide)

<figure class="featured">
<img src="https://allthingsopen.org/wp-content/uploads/2026/06/coding-laptop-keyboard-e1780974871141.jpg" class="featured" alt="Computer code on a blurred laptop screen with a focus on the A Z X keys on a black keyboard" />
<figcaption>Image by <a href="https://pixabay.com/users/stocksnap-894430/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=926242">StockSnap</a> from <a href="https://pixabay.com//?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=926242">Pixabay</a></figcaption>
</figure>

There’s a lot of pushback on artificial intelligence in education. Many educators worry that AI threatens learning and that students will simply copy generated code rather than understand it. Should we ban AI from the classroom? Or should we embrace it as a teaching tool?

The answer is neither. We should use AI as a “tutor on demand.”

When a friend who was learning Python asked me to review her code for a tool assessing artificial intelligence’s impact on small businesses, it made me reconsider how I teach Python. How could I use AI not as a replacement for learning, but as a partner in it?

## Using AI as a Socratic tutor for Python

Rather than banning AI from the classroom, educators can leverage it as a Socratic assistant. Instead of asking AI to “*fix this code*,” encourage students to ask AI specific questions like “*Why is this loop not working?*” or “*What does this variable store?*“

This approach fundamentally changes the learning dynamic. Students engage more deeply with the underlying logic. They learn to ask better questions, think critically about their problems, and understand the “why” behind solutions rather than just the “what.”

By framing AI as a tutor that asks questions in return, you shift the power dynamic. Students become active learners asking for explanations, not passive recipients of generated code.

## Teaching critical evaluation and code quality

It’s crucial to help students understand that generative AI doesn’t guarantee correctness. AI can introduce subtle logical errors, performance issues, or inefficient approaches. Students need to learn how to evaluate the code AI generates.

Teach students to:

- Test their code thoroughly
- Ask “*Does this actually solve the problem?*“
- Compare different solutions and understand trade-offs
- Recognize when AI suggestions might be suboptimal

This critical lens transforms AI from a shortcut into a learning tool that teaches discernment.

**Read more: <a href="https://allthingsopen.org/articles/5-common-mistakes-new-linux-users" id="8882" type="articles" target="_blank" rel="noreferrer noopener">The 5 most common mistakes new Linux users make</a>**

## Learning through multiple solutions

One of AI’s greatest strengths in education is showing students that multiple approaches exist to solve the same problem. A simple task like drawing a circle in Python can be done several ways.

I once asked an AI agent: “Draw a circle with Python.” I was thinking of the <a href="https://docs.python.org/3/library/turtle.html" target="_blank" rel="noreferrer noopener">turtle</a> module, but the AI generated code using <a href="https://matplotlib.org/" target="_blank" rel="noreferrer noopener">matplotlib</a> instead:

``` wp-block-prismatic-blocks
import matplotlib.pyplot as plt

# Create a figure and an axis
fig, ax = plt.subplots()

# Create a circle patch (Center: x=0, y=0, Radius=5)
circle = plt.Circle((0, 0), 5, color='blue', fill=False, linewidth=2)

# Add the circle to the axis
ax.add_patch(circle)

# Set equal scaling so the circle is not distorted into an oval
ax.set_aspect('equal', adjustable='datalim')

# Automatically scale the plot limits to show the circle
ax.autoscale_view()

# Display the plot
plt.title("Circle using Matplotlib")
plt.grid(True)
plt.show()
```

<div class="wp-block-image">

<figure class="aligncenter size-full">
<img src="https://allthingsopen.org/wp-content/uploads/2026/06/matplotlib-blue-circle.png" class="wp-image-9024" data-fetchpriority="high" decoding="async" srcset="https://allthingsopen.org/wp-content/uploads/2026/06/matplotlib-blue-circle.png 533w, https://allthingsopen.org/wp-content/uploads/2026/06/matplotlib-blue-circle-300x236.png 300w" sizes="(max-width: 533px) 100vw, 533px" width="533" height="420" alt="matplotlib blue circle graph python example" />
<figcaption>Screen capture by Don Watkins CC-BY-SA 4.0</figcaption>
</figure>

</div>

I wouldn’t have thought of that approach on my own. This is powerful: Students can see that there are always multiple valid solutions, each with different trade-offs. This expands their thinking and shows them the breadth of Python’s ecosystem.

**Read more: <a href="https://allthingsopen.org/articles/what-to-do-when-ai-starts-going-in-circles" id="8800" type="articles" target="_blank" rel="noreferrer noopener">What to do when your AI starts going in circles</a>**

## Open source tools for teaching Python

Making programming accessible and engaging matters. The combination of AI with open source tools ensures students learn effectively while enjoying the process.

<a href="https://vscodium.com/" target="_blank" rel="noreferrer noopener">VSCodium</a> (an open source version of Visual Studio Code) is lightweight and works well with AI assistants. <a href="https://thonny.org/" target="_blank" rel="noreferrer noopener">Thonny</a> is specifically designed for beginners, with a built-in Python interpreter and visual debugging. <a href="https://codewith.mu/" target="_blank" rel="noreferrer noopener">Mu</a> provides a simple, distraction-free environment perfect for learning.

These tools, combined with thoughtful use of AI, create an engaging learning environment where students can experiment freely without cost or complexity.

## The future of Python education

Rather than viewing AI as a threat to learning, embrace its potential to enhance teaching. AI can make programming education more accessible, more engaging, and more effective when used thoughtfully.

The goal isn’t to replace human instruction. It’s to create a learning environment where students explore concepts deeply, ask better questions, and understand not just how to code, but why different solutions exist. Through collaborative exploration with AI as a tool, you cultivate programmers who are skilled, thoughtful, and ready to innovate.

## More from We Love Open Source

- <a href="http://allthingsopen.org/articles/15-open-source-backup-solutions-2026" target="_blank" rel="noreferrer noopener">15 open source backup solutions to protect your data</a>
- <a href="https://allthingsopen.org/articles/5-common-mistakes-new-linux-users" id="8882" type="articles" target="_blank" rel="noreferrer noopener">The 5 most common mistakes new Linux users make</a>
- <a href="http://allthingsopen.org/articles/ai-slop-problem-open-source-maintainers" target="_blank" rel="noreferrer noopener">The AI slop problem threatening open source maintainers</a>
- <a href="https://allthingsopen.org/articles/what-to-do-when-ai-starts-going-in-circles" id="8800" type="articles" target="_blank" rel="noreferrer noopener">What to do when your AI starts going in circles</a>
- <a href="http://allthingsopen.org/articles/5-forces-driving-devops-ai-2026" target="_blank" rel="noreferrer noopener">5 forces driving DevOps and AI in 2026</a>

This article is adapted from “<a href="https://donwatkins.info/2026/06/05/teaching-python/" target="_blank" rel="noreferrer noopener"><em>Teaching Python</em></a>” by Don Watkins, and is republished with permission from the author.

</div>

---

<div class="cc-license">

<a href="https://creativecommons.org/licenses/by-sa/4.0/" rel="license"><img src="https://allthingsopen.org/wp-content/themes/ato-main-2024/img/cc/by-sa.png" title="This work is licensed under a Creative Commons Attribution-Share Alike 4.0 International License." alt="Creative Commons License" /></a>

This work is licensed under a Creative Commons Attribution-Share Alike 4.0 International License.

