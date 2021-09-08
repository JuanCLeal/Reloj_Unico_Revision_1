bajada_posicion = 0

def setup():
    size(700, 500)
    
def draw():
    global bajada_posicion
    
    background(175)
    
    ellipse(200, bajada_posicion,50,50)
    
    if bajada_posicion > height:
        bajada_posicion = 0
    else:
        bajada_posicion = map(hour(), 0, 24, 0, height)