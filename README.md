# Murder-Mystery-Story

def setup():

#code for the final verdict screen
  def verdictScreen():
    office = loadImage("office2.jpg") #the image is on my desktop
    size(800,533)
    image(office,0,0,800,533)
    textSize(50)
    text("The Killer is...") 



#code for questions and answers screen
  def qna():
      size(800,533)
      background(0,0,0)
      name = "Name of the game"
      
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
    
      #Red Score Box 
      stroke(255,255,255)
      fill(255,0,0)
      rect(740,180,40,40)
    
      fill(0,0,0)
    
      #Red Score 
      textSize(30)
      textAlign(CENTER)
      text("0",760,210)
    
      #Green Score Box 
      stroke(255,255,255)
      fill(0,255,0)
      rect(740,240,40,40)
    
      fill(0,0,0)
    
      #Green Score 
      textSize(30)
      textAlign(CENTER)
      text("0",760,270)
    
      #Blue Score Box 
      stroke(255,255,255)
      fill(0,0,255)
      rect(740,300,40,40)
    
      fill(0,0,0)
      
      #Blue Score 
      textSize(30)
      textAlign(CENTER)
      text("0",760,330)
      
      #Red Choice Box 
      stroke(255,255,255)
      fill(255,0,0)
      rect(80,440,70,70)
    
      #Green Choice Box 
      stroke(255,255,255)
      fill(0,255,0)
      rect(360,440,70,70)
      
      #Blue Choice Box 
      stroke(255,255,255)
      fill(0,0,255)
      rect(640,440,70,70)
    
      fill(255,255,255)
  # code for title screen
 def setup():
    size(800,533)
    global img
    img= loadImage ("House.jpg")
def draw():
    global img
    img= loadImage ("House.jpg")
    background(img)
    textSize(30)
    fill(255,255,255)
    text("CSSI Murder Mysteries",250,50)
    fill(0)
    rect(250,460,300,50)
    textSize(30)
    fill(255,255,255)
    text("Click screen to begin", 250,460,350,50) 
