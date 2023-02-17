# Next To

<br />
<br />



https://user-images.githubusercontent.com/112841868/219572842-383832db-2f8f-4933-a646-3b509e8a1d14.mp4

```python
from manim import *


class MessingAround(Scene):
    def construct(self):

class MessingAround(Scene):
    def construct(self):

        # Mobject

        plane = NumberPlane()
        point_A = Dot(color = WHITE)
        point_B = Dot(color = RED)
        point_C = Dot(color = BLUE)
        point_D = Dot(color = GREEN)
        point_E = Dot(color = YELLOW)        

        Direction = [RIGHT, UP, LEFT, DOWN]
        MyPoints = [point_A, point_B, point_C, point_D, point_E]

        # Positions 

        for x in range(len(Direction)):
            MyPoints[x+1].next_to(point_A,Direction[x])


        # Display

        self.add(plane)
        for x in MyPoints:
            self.play(
            FadeIn(x),
            run_time = 1
        )               
        self.wait(1)
```

<br />
<br />

# Shift

<br />
<br />


https://user-images.githubusercontent.com/112841868/219577257-e263340e-fe87-49a4-a132-2cecc18caa21.mp4

```python

from manim import *


class MessingAround(Scene):
    def construct(self):

        # Mobject

        plane = NumberPlane()
        point_A = Dot(color = WHITE)
        point_B = Dot(color = RED)
        point_C = Dot(color = BLUE)
        point_D = Dot(color = GREEN)
        point_E = Dot(color = YELLOW)        

        MyPoints = [point_A, point_B, point_C, point_D, point_E]

        # Positions 

        for x in range(len(MyPoints))  :
            MyPoints[x].shift(RIGHT*x)


        # Display

        self.add(plane)
        for x in MyPoints:
            self.play(
            FadeIn(x),
            run_time = 1
        )               
        self.wait(1)
```
<br />
<br />

# MoveTo

<br />
<br />

https://user-images.githubusercontent.com/112841868/219578446-fd1af99f-61b1-4dcd-a49a-a48cf446f38a.mp4


```python 

from manim import *


class MessingAround(Scene):
    def construct(self):

        # Mobject

        plane = NumberPlane()
        point_A = Dot(color = WHITE)
        point_B = Dot(color = RED)
        point_C = Dot(color = BLUE)
        point_D = Dot(color = GREEN)
        point_E = Dot(color = YELLOW)        

        MyPoints = [point_A, point_B, point_C, point_D, point_E]

        # Positions 

        for x in range(len(MyPoints))  :
            MyPoints[x].move_to([x,x,0])


        # Display

        self.add(plane)
        for x in MyPoints:
            self.play(
            FadeIn(x),
            run_time = 1
        )               
        self.wait(1)
```

<br />
<br />

# AlignTo

<br />
<br />



https://user-images.githubusercontent.com/112841868/219589363-d171911e-6263-4d64-a20a-87fb3070f83d.mp4




```python
from manim import *


class MessingAround(Scene):
    def construct(self):

        # Mobject

        plane = NumberPlane()
        point_A = Dot(color = WHITE)
        point_B = Dot(color = RED)
        point_C = Dot(color = BLUE)
        point_D = Dot(color = GREEN)
        point_E = Dot(color = YELLOW)        

        point_A1 = Dot(color = WHITE)
        point_B1 = Dot(color = RED)
        point_C1 = Dot(color = BLUE)
        point_D1 = Dot(color = GREEN)
        point_E1 = Dot(color = YELLOW)        

        MyPoints = [point_A, point_B, point_C, point_D, point_E]
        MyPointsCopy = [point_A1, point_B1, point_C1, point_D1, point_E1]

        # Positions 

        for x in range(len(MyPoints))  :
            MyPoints[x].move_to([x,x,0])
            MyPointsCopy[x].move_to([x,x,0])
        # Display

        self.add(plane,point_A,point_B,point_C,point_D,point_E)

        for x in range(len(MyPoints))  :
            self.play(

                Transform(MyPoints[x],MyPointsCopy[x].align_to(point_C,RIGHT)),
                run_time = 0.5

            )
        for x in range(len(MyPoints))  :
            self.play(

                Transform(MyPoints[x],MyPointsCopy[x].align_to(point_C,UP)),
                run_time = 0.5

            )            
        self.wait(1)
```

<br />
<br />

# Arrange

<br />
<br />



https://user-images.githubusercontent.com/112841868/219592989-c4164a4d-682d-4ea9-8c20-439673a6afff.mp4


```python

from manim import *


class MessingAround(Scene):
    def construct(self):

        # Mobject

        plane = NumberPlane()
        point_A = Dot(color = WHITE)
        point_B = Dot(color = RED)
        point_C = Dot(color = BLUE)
        point_D = Dot(color = GREEN)
        point_E = Dot(color = YELLOW)        

        points = VGroup(point_A, point_B, point_C, point_D, point_E)
        

        # Positions 

        points.arrange(RIGHT)


        # Display

        self.add(plane)
        self.play(

            Create(points),
            run_time = 6
        )
```
<br />
<br />

# Rotate 

<br />
<br />



https://user-images.githubusercontent.com/112841868/219606984-ab1eccb5-5b78-4040-9545-343d8ce0e196.mp4

```python3
from manim import *


class MessingAround(Scene):
    def construct(self):

        # Mobject
        arrow_1 = Arrow(start=DOWN, end=UP, color=WHITE)
        arrow_2 = Arrow(start=DOWN, end=UP, color=RED)
        arrow_3 = Arrow(start=DOWN, end=UP, color=BLUE)
        arrow_4 = Arrow(start=DOWN, end=UP, color=GREEN)
        arrow_5 = Arrow(start=DOWN, end=UP, color=YELLOW)

        Arrows = VGroup (arrow_1,arrow_2,arrow_3,arrow_4,arrow_5).arrange(RIGHT, buff = 2)

        # Display 

        self.play(

            Rotate(Arrows[0],PI,rate_func = lambda t: t ),
            Rotate(Arrows[1],PI,rate_func = smooth ),
            Rotate(Arrows[2],PI,rate_func = lambda t: np.sin(t*PI) ),
            Rotate(Arrows[3],PI,rate_func = lambda t: t*2),
            Rotate(Arrows[4],PI,rate_func = lambda t: 1 - abs((1 - 2*t))),
            run_time = 6

        )
       
```
