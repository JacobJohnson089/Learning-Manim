# Memory Visualization


https://user-images.githubusercontent.com/112841868/219785087-84901f9e-fc67-4fd4-ba7a-26170383cf45.mp4

```python
from manim import *


class MessingAround(Scene):
    def construct(self):

        # Mobjects

        arrow = Arrow(start=DOWN, end=UP, color=YELLOW)

        Address = VGroup(
            Text("0", font= "Mona Sans",font_size=30,color = BLUE),
            Text("0", font= "Mona Sans",font_size=30,color = BLUE),
            Text("0", font= "Mona Sans",font_size=30,color = BLUE),
            Text("0", font= "Mona Sans",font_size=30,color = BLUE),
            Text("0", font= "Mona Sans",font_size=30,color = BLUE),
            Text("0", font= "Mona Sans",font_size=30,color = BLUE),
            Text("0", font= "Mona Sans",font_size=30,color = BLUE),
            Text("0  ", font= "Mona Sans",font_size=30,color = BLUE))
        
        

        #Memory = Text("00", font_size= 24, font="Mona Sans")

        Memory = VGroup()
        for x in range(16):
            Memory.add(Text("00", font_size= 24, font="Mona Sans",color=RED))


        # Transformations



        Address.arrange(RIGHT,buff = 0.25)
        Address[7].next_to(Address[6],RIGHT, buff= -0.25)
        Address.shift(UP * 2)


        arrow.move_to([-4,-1,0])


        for x in range(8):
            Memory[x-1].move_to([(-4+(x/2)),0,0])
        for x in range(8):
            Memory[x+8-1].move_to([(0.5+(x/2)),0,0])
        

        # Display

        self.play(

            Create(Text("How to read memory addresses"))
        )
        self.wait(1)
        self.clear()

        for x in range(8):

            
            Address[7] = Text(str(x), font= "Mona Sans",font_size=30,color=BLUE)
            Address[7].next_to(Address[6],RIGHT)
            
            
            self.add(Address, Memory,arrow)
            self.play(
                
                arrow.animate.shift(RIGHT*0.5),
            )
        self.play(
                
                arrow.animate.shift(RIGHT*0.5),
            )
        for x in range(2):

            
            Address[7] = Text(str(x+8), font= "Mona Sans",font_size=30,color=BLUE)
            Address[7].next_to(Address[6],RIGHT)
            
            
            self.add(Address, Memory,arrow)
            self.play(
                
                arrow.animate.shift(RIGHT*0.5),
            )
        for x in range(6):

            Hex_Char = ["A","B","C","D","E","F"]
            Address[7] = Text(str(Hex_Char[x]), font= "Mona Sans",font_size=30,color=BLUE)
            Address[7].next_to(Address[6],RIGHT)
            
            
            self.add(Address, Memory,arrow)
            self.play(
                
                arrow.animate.shift(RIGHT*0.5),
            )
        
        Address[6] = Text(str(1), font= "Mona Sans",font_size=30,color=BLUE)
        Address[6].next_to(Address[5],RIGHT)
        Address[7] = Text(str(0), font= "Mona Sans",font_size=30,color=BLUE)
        Address[7].next_to(Address[6],RIGHT)            
            
        self.add(Address, Memory,arrow)
        self.play(arrow.animate.move_to([-4,-1,0]))
        self.wait(2)

        
        
        


```
