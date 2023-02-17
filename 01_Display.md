# Create

<br />
<br />



https://user-images.githubusercontent.com/112841868/219556110-f949870f-7ff3-4a07-aae2-2068b07d8b5b.mp4

```python
from manim import *


class Create(Scene):
    def construct(self):

        # Creating Mobjects

        circle = Circle(

            radius=1,
            color=RED,

        )
        

        # Displaying Mobjects

        self.play(

            Create(circle),
            run_time = 5     
            
            )
        self.wait(1)


```

<br />
<br />

# FadeIn

<br />
<br />

https://user-images.githubusercontent.com/112841868/219556271-e2c716b9-2ae7-434e-9b32-dc16d75e08a5.mp4

```python
from manim import *


class FadeIn(Scene):
    def construct(self):

        # Creating Mobjects

        circle = Circle(

            radius=1,
            color=RED,


        )
        

        # Displaying Mobjects

        self.play(

            FadeIn(circle),
            run_time = 5     
            
            )
        self.wait(1)


```

<br />
<br />

# DrawBorderThenFill

<br />
<br />

https://user-images.githubusercontent.com/112841868/219557669-aff488ed-0ffb-440d-a490-961200104337.mp4

```python
from manim import *


class MessingAround(Scene):
    def construct(self):

        # Creating Mobjects

        circle = Circle(

            radius=1,
            color=RED,
            fill_opacity = 0.5

        )
        

        # Displaying Mobjects

        self.play(

            DrawBorderThenFill(circle),
            run_time = 5     
            
            )
        self.wait(1)

```
<br />
<br />

# Transform

<br />
<br />

https://user-images.githubusercontent.com/112841868/219561615-6ccee436-ba64-453b-9a48-74139a0636a9.mp4

```python

from manim import *


class MessingAround(Scene):
    def construct(self):

        # Creating Mobjects

        square =Square(

            side_length=1,
            color=RED,
            fill_opacity = 0.5

        )

        circle = Circle(

            radius=1,
            color=GREEN,
            fill_opacity = 0.5

        )

        triangle = Triangle(


            color=BLUE,
            fill_opacity = 0.5

        )        

    
        

        # Displaying Mobjects

        self.play(

            Transform(square, circle),
            run_time = 2.5
        )
        self.clear()
        self.play(

            Transform(circle, triangle),
            run_time = 2.5
        )


        
        self.wait(1)
```



