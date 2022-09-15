# Turtle_Random_Walk
More fun with the Turtle module. Moving in random directions and drawing with random colors makes a pretty picture.

tim = Turtle()
screen = Screen()

tim.shape("turtle")
tim.color("yellow")
tim.pensize(5)

colors = ["red", "blue", "yellow", "green", "orange", "purple", "black", "cyan", "pink"]
directions = ["right", "left", "forward", "backward"]

for _ in range(1000):
    chosen_color = random.choice(colors)
    tim.color(chosen_color)
    choice_of_direction = random.choice(directions)
    if random.choice(directions) == "right":
        tim.right(90)
        tim.forward(10)
    elif random.choice(directions) == "left":
        tim.left(90)
        tim.forward(10)
    elif random.choice(directions) == "forward":
        tim.forward(10)
    else:
        tim.backward(10)

screen.exitonclick()

