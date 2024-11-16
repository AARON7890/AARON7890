import turtle
import random
import time

wn = turtle.Screen()
wn.title("jumping")
wn.bgcolor("black")
wn.setup(800,600)
wn.tracer(0)


player = turtle.Turtle()
player.speed(0)
player.shape("circle")
player.color("blue")
player.penup()
player.goto(-350, -250)

paddle = turtle.Turtle()
paddle.speed(0)
paddle.shape("square")
paddle.color("orange")
paddle.shapesize(stretch_wid=20, stretch_len=1)
paddle.penup()
paddle.goto(0,0)

paddle = turtle.Turtle()
paddle.speed(0)
paddle.shape("square")
paddle.color("orange")
paddle.shapesize(stretch_wid=20, stretch_len=1)
paddle.penup()
paddle.goto(350 ,0)


def player_up():
    y = player.ycor()
    y += 20
    player.sety(y)

def player_down():
    y = player.ycor()
    y -= 20
    player.sety(y)

def player_left():
    x = player.xcor()
    x += 20
    player.setx(x)

def player_right():
    x = player.xcor()
    x -= 20
    player.setx(x)

wn.listen()
wn.onkeypress(player_up, "Up")
wn.onkeypress(player_down, "Down")
wn.onkeypress(player_left, "Left")
wn.onkeypress(player_right, "Right")

while True:
    wn.update()
