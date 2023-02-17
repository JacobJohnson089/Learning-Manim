# Environment

<br />
<br />

```python
from manim import *


class name_of_animation(Scene):
  def construct(self):
  
      # Your code
  
  ```
  
  <br />
  <br />
  
  # Creating Mobjects
  
  <br />
  <br />
  
  ```python
  
  variable_name = Mobject(
  
      Parameters
      
      )
      
      
 # e.g 
 
         axes = Axes(

            x_range=(-3, 3),
            y_range=(-3, 3),
            
            )
```

  <br />
  <br />
  
  # Displaying Mobject
  
  <br />
  <br />
  
  ```python
  
  self.play(

            Create(area),
            run_time = 5

        )
 ```
 
 <br />
 <br />
 
 # Exemple
 
 <br />
 <br />
 
 ```python
 
 class MessingAround(Scene):
    def construct(self):

        # Creating Mobjects

        axes = Axes(

            x_range=(-3, 3),
            y_range=(-3, 3),
            
            )

        curve = axes.plot(

            lambda x:(x+2)*x*(x-2)/2,
            color=RED
            
            )

        area = axes.get_area(
            
            curve, (-2,0) 

            )
        

        # Displaying Mobjects

        self.play(

            Create(axes),
            Create(curve),
            Create(area),
            run_time = 10     
            
            )
            
  ```
  
  
 
 
 
 
 
 

https://user-images.githubusercontent.com/112841868/219555110-da452d4b-22fe-45f1-9874-e6d9e13c3d03.mp4


 
 
  
  
  
  
