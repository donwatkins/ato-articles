# Explore the intersection of programming and mathematics with Turtle graphics

Create vector graphics using this open source Python module.

**By Don Watkins**  
**Published:** June 26, 2024  
**Source:** [https://allthingsopen.org/articles/turtle-graphics](https://allthingsopen.org/articles/turtle-graphics)

<figure class="featured">
<img src="https://allthingsopen.org/wp-content/uploads/2024/06/math-science-graphs-e1718733350834.jpg" class="featured" alt="Graphic artwork with science and math notes." />
<figcaption>Image by <a href="https://pixabay.com/users/marijana1-8558212/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=3480102">Marijana</a> from <a href="https://pixabay.com//?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=3480102">Pixabay</a></figcaption>
</figure>

Mathematics was anathema to me in my early years. As a visual learner, abstract concepts were challenging for me. However, in graduate school, I had to teach a fifth-grade student geometry using a unique curriculum involving Apple Logo and Turtle graphics. This experience changed my perspective on math.

My transformative journey with Turtle graphics began about nine years ago when I serendipitously discovered the ‘Turtle’ module for Python at a workshop. Python is readily available on most Linux distributions, so I eagerly embraced the Turtle. Learning to <a href="https://docs.python.org/3/library/turtle.html#module-turtle" target="_blank" rel="noreferrer noopener nofollow">use the ‘turtle’ module</a> introduced me to Python and opened up a world of creativity and learning. I’ve been fortunate to share this journey with others, especially young people eager to create turtle graphics and explore the fascinating intersection of programming and mathematics.

My first experiences with Python began in the terminal and the REPL (read eval print-loop).

<div class="wp-block-image">

<figure class="aligncenter size-full">
<img src="http://allthingsopen.org/wp-content/uploads/2024/06/turtle-graphics-01.png" class="wp-image-5276" data-fetchpriority="high" decoding="async" srcset="https://allthingsopen.org/wp-content/uploads/2024/06/turtle-graphics-01.png 719w, https://allthingsopen.org/wp-content/uploads/2024/06/turtle-graphics-01-300x57.png 300w" sizes="(max-width: 719px) 100vw, 719px" width="719" height="136" alt="Importing Turtle via Python on the command line" />
<figcaption>CC-BY-SA 4.0 by Don Watkins</figcaption>
</figure>

</div>

Keeping things simple, I begin with a program to draw a square. I need to add a couple of lines of code to keep the window open so I can show the students the code and they can see the graphical representation. I teach the students the importance of adding comments to their code, which helps them remember what each code block is for and explain what is happening to others they might be sharing their code with. Comments are denoted with the hash ‘`#`‘

That code is:

``` wp-block-prismatic-blocks
# This is the code to add the turtle library

import turtle

# This is the code to add the drawing window

window = turtle.Screen()

# This is the code to close the drawing window

window.exitonclick()
```

Next, I showed them how to draw a simple square using a turtle. 

``` wp-block-prismatic-blocks
# This is the code to import the turtle function

import turtle

# This is the code to open the drawing window

window = turtle.Screen()

# This is the code to draw the square

turtle.forward(100)
turtle.right(90)
turtle.forward(100)
turtle.right(90)
turtle.forward(100)
turtle.right(90)
turtle.forward(100)
turtle.right(90)

# This is the code to close the window

window.exitonclick()
```

<div class="wp-block-image">

<figure class="aligncenter size-full">
<img src="http://allthingsopen.org/wp-content/uploads/2024/06/turtle-graphics-02.png" class="wp-image-5275" decoding="async" srcset="https://allthingsopen.org/wp-content/uploads/2024/06/turtle-graphics-02.png 822w, https://allthingsopen.org/wp-content/uploads/2024/06/turtle-graphics-02-300x211.png 300w, https://allthingsopen.org/wp-content/uploads/2024/06/turtle-graphics-02-768x540.png 768w" sizes="(max-width: 822px) 100vw, 822px" width="822" height="578" alt="Turtle graphics example: Square" />
<figcaption>CC-BY-SA 4.0 by Don Watkins</figcaption>
</figure>

</div>

I show them how to simplify and iterate their code using a ‘for’ loop. The ‘for’ loop produces the same square as illustrated above but with far less code.

``` wp-block-prismatic-blocks
# import the turtle function
import turtle

# This is the code to open the drawing window
window = turtle.Screen()

# The range function to create the square

for x in range(4):
 turtle.forward(100)
 turtle.right(90)

# This is the code to close the window

window.exitonclick()
```

I show them how to give the ‘turtle’ different names and create more than one turtle. I introduce the students to objects and show them how to create a unique ‘turtle’ object using a name. In this case I will use the name ‘jeff.’ All of these iterations produce the same figure illustrated above but are building blocks for later use.

``` wp-block-prismatic-blocks
# import the turtle function

import turtle

# Create a separate turtle named jeff

jeff = turtle.Turtle()

# This is the code to open the drawing window

window = turtle.Screen()

for x in range(4):
 jeff.forward(100)
 jeff.right(90)

# Code to close the drawing window

window.exitonclick()
```

I demonstrate that we can create a simple square spiral by changing our code slightly.

``` wp-block-prismatic-blocks
# import the turtle function

import turtle

# Create a separate turtle named jeff

jeff = turtle.Turtle()

# This is the code to open the drawing window

window = turtle.Screen()

for x in range(4):
 jeff.forward(100)
 jeff.right(90)

# Code to close the drawing window

window.exitonclick()
```

<div class="wp-block-image">

<figure class="aligncenter size-full">
<img src="http://allthingsopen.org/wp-content/uploads/2024/06/turtle-graphics-03.png" class="wp-image-5274" decoding="async" srcset="https://allthingsopen.org/wp-content/uploads/2024/06/turtle-graphics-03.png 816w, https://allthingsopen.org/wp-content/uploads/2024/06/turtle-graphics-03-300x291.png 300w, https://allthingsopen.org/wp-content/uploads/2024/06/turtle-graphics-03-768x745.png 768w" sizes="(max-width: 816px) 100vw, 816px" width="816" height="792" alt="Turtle graphics example graph" />
<figcaption>CC-BY-SA 4.0 by Don Watkins</figcaption>
</figure>

</div>

I gradually introduced more complexity in each of the programming examples and then let the students’ imaginations and nascent programming run wild. In the code below, I have added ‘color’, ‘pensize’, and ‘speed’ iterations to the code, along with changing the range and the distance the ‘turtle’ moves forward. The ‘speed’ is set to zero, the fastest drawing speed available.

``` wp-block-prismatic-blocks
# import the turtle function

import turtle

# code to create drawing window

window = turtle.Screen()

# Create a separate turtle object with colors and details

jeff = turtle.Turtle()
jeff.color("blue")
jeff.pensize(3)
jeff.speed(0)

for x in range(50):
 jeff.forward(200)
 jeff.right(92)

window.exitonclick()
```

<div class="wp-block-image">

<figure class="aligncenter size-full">
<img src="http://allthingsopen.org/wp-content/uploads/2024/06/turtle-graphics-04.png" class="wp-image-5273" decoding="async" srcset="https://allthingsopen.org/wp-content/uploads/2024/06/turtle-graphics-04.png 766w, https://allthingsopen.org/wp-content/uploads/2024/06/turtle-graphics-04-300x284.png 300w" sizes="(max-width: 766px) 100vw, 766px" width="766" height="724" alt="Turtle graphics example: Blue graphic" />
<figcaption>CC-BY-SA 4.0 by Don Watkins</figcaption>
</figure>

</div>

Many options within the ‘turtle’ library provide many opportunities to work with beginning programmers. There are endless possibilities when you use Python and other open source tools combined with your imagination and those of your students. Here’s one final code snippet that demonstrates more complex Python programming.

``` wp-block-prismatic-blocks
# Draw a circle spiral with four colors

# import the turtle function

import turtle

# create the drawing window

window = turtle.Screen()

# set the drawing speed to zero which is the fastest

turtle.speed(0)

# list the colors in the circle spiral

colors = ["red", "brown", "blue", "green"]

for x in range(100):
  turtle.pencolor(colors[x%4])
  turtle.circle(x)
  turtle.left(91)

# close the drawing window

window.exitonclick()
```

<div class="wp-block-image">

<figure class="aligncenter size-full">
<img src="http://allthingsopen.org/wp-content/uploads/2024/06/turtle-graphics-05.png" class="wp-image-5272" decoding="async" srcset="https://allthingsopen.org/wp-content/uploads/2024/06/turtle-graphics-05.png 952w, https://allthingsopen.org/wp-content/uploads/2024/06/turtle-graphics-05-300x281.png 300w, https://allthingsopen.org/wp-content/uploads/2024/06/turtle-graphics-05-768x720.png 768w" sizes="(max-width: 952px) 100vw, 952px" width="952" height="892" alt="Turtle graphics example: 3 dimensional graphic" />
<figcaption>CC-BY-SA 4.0 by Don Watkins</figcaption>
</figure>

</div>

Turtle graphics is not just a tool for executing commands but a gateway to encourage students to think procedurally and reflect on their thought processes. It provides instant visual feedback on code, allowing students to explore mathematical concepts and unleash creativity. You can easily see that Python Turtle graphics are a great example of open source’s power to provide an extremely affordable, world-class programming environment.

</div>

---

<div class="cc-license">

<a href="https://creativecommons.org/licenses/by-sa/4.0/" rel="license"><img src="https://allthingsopen.org/wp-content/themes/ato-main-2024/img/cc/by-sa.png" title="This work is licensed under a Creative Commons Attribution-Share Alike 4.0 International License." alt="Creative Commons License" /></a>

This work is licensed under a Creative Commons Attribution-Share Alike 4.0 International License.

