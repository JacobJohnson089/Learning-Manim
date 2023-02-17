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
  
  
  
  
