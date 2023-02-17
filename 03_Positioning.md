# Next To

<br />
<br />



https://user-images.githubusercontent.com/112841868/219572842-383832db-2f8f-4933-a646-3b509e8a1d14.mp4

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


        # Code

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
