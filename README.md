bajada_posicion = 0
vertical_position = 0

def setup():
    size(700, 500)
    
def draw():
    global bajada_posicion
    global vertical_position

    background(175)
    
    ellipse(200, bajada_posicion,50,50)

    if bajada_posicion > height:
        bajada_posicion = 0
    else:
        bajada_posicion = map(hour(), 0, 24, 0, height)

    ellipse(400, vertical_position, 50, 50)
    
    if vertical_position > height:
        vertical_position = 0
    else:
        vertical_position = map(minute(), 0, 59, 0, height)