reloj unico

vertical_position = 0
vertical_position1 = 0
vertical_position2 = 0
def setup():
    size(600, 250)
    background(10)
def draw():
    global vertical_position
    global vertical_position1
    global vertical_position2
    background (map(second(), 0, 59, 250, 0))
    if vertical_position > height:
        vertical_position = 0
    else:
        vertical_position = map(second(), 0, 59, 0, height)
        
    if vertical_position1 > height:
        vertical_position1 = 0
    else:
        vertical_position1 = map(minute(), 0, 59, 0, height)
        
        
    if vertical_position2 > height:
        vertical_position2 = 0
    else:
        vertical_position2 = map(hour(), 0, 23, 0, height)

    fill(300,200,56)
    ellipse(300, vertical_position1, 55, 55)
    fill(355,100,67)
    ellipse(150, vertical_position2, 55, 55)
    fill(58,66,100)
    ellipse(450, vertical_position, 55, 55)
    stroke(350)