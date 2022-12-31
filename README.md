# heart
#make heart using turtle &amp; math module using normal trigo functions
#by Ayush Dubey

import turtle
import math


def lovecurve(t):
    x=16*(math.sin(t)**3) #defining the goto coordinates of x
    y=13*math.cos(t)-5*math.cos(2*t)-2*math.cos(3*t)-math.cos(4*t) # goto coordinates of y
    return x,y

turtle.setup(800,800)  # screen size
turtle.title("My Heart is your ;)") #title
turtle.bgcolor("black")  # back screen colour
turtle.pensize(2) # recomended
turtle.pencolor("red") # colour of the precious gift ;)
turtle.speed(0.1) 

factor = 20 #multiple
turtle.penup()
for i in range(0,400):
    x,y=lovecurve(i)
    turtle.goto(x*factor,y*factor)
    turtle.pendown()

turtle.getcanvas().postscript(file="lovedrawing.eps")
turtle.exitonclick()
