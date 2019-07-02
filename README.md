# Murder-Mystery-Story


#code for the final verdict screen
def verdictScreen():
  office = loadImage("office2.jpg") #the image is on my desktop
  size(800,533)
  image(office,0,0,800,533)
  textSize(50)
  text("The Killer is...") 




def setup():
    size(800,533)
    background(0,0,0)
    name = "Name of the game" 
def draw():
    background(0)
    textSize(40)
    textAlign(CENTER)
    text("Name of Game",400,60)
    
    textSize(20)
    textAlign(CENTER)
    text("Question?", 400,160)
    
    textSize(20)
    textAlign(CENTER)
    text("Response",400,260)
    
    textSize(20)
    textAlign(CENTER)
    text("Who do you suspect the most?", 400, 360)
    
    stroke(255,255,255)
    fill(255,0,0)
    rect(740,180,40,40)
    
    fill(0,0,0)
    
    textSize(30)
    textAlign(CENTER)
    text("0",760,210)
    
    stroke(255,255,255)
    fill(0,255,0)
    rect(740,240,40,40)
    
    fill(0,0,0)
    
    textSize(30)
    textAlign(CENTER)
    text("0",760,270)
    
    stroke(255,255,255)
    fill(0,0,255)
    rect(740,300,40,40)
    
    fill(0,0,0)
    
    textSize(30)
    textAlign(CENTER)
    text("0",760,330)
    
    stroke(255,255,255)
    fill(255,0,0)
    rect(80,440,70,70)
    
    stroke(255,255,255)
    fill(0,255,0)
    rect(360,440,70,70)
    
    stroke(255,255,255)
    fill(0,0,255)
    rect(640,440,70,70)
    
    fill(255,255,255)
