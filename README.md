# Murder-Mystery-Story

def setup():
  size(800,533)
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
    
    
    POV = { 
    
    "questions" : ["Where were you between 1:30 - 2:30 am on Saturday morning?", "What was your relationship with the victim?", "What was the last conversation you had with the victim?", "Who do you suspect?"], 
    
    "Shelby": [
    “My campaign manager, my son and I were talking on the couch about the banquet when Connor, you know my son Connor, went to the bathroom. Right after Ray Ray said he went to his car and I went to my office. It was maybe 10 minutes later when I heard the maid scream.”, 
    
    “He was exactly what the title suggested, my campaign manager, nothing more, nothing less.”, 
    
    “Our last private conversation had a lot to do with the future. Things such as re-election and if I’d ever run for a higher position in office. I told him let’s start off small, but he insisted. When I declined, he asked for a raise, so I cut the conversation short.”, 
   
   “The Maid because I would always find her and Ray Ray in compromising situations; they seemed fairly comfortable with each other.”]
    , 

  "Connor":[ 
  
  "My mom, Ray Ray and I were chilling on the couch. When I got up to go make a call in my room. After the call I was making my way back to the drawing room and got halfway down the stairs when I heard a scream.”,

“I didn’t know much about him, seemed like a cool guy. He even hand delivered my invitation to me, so clearly he was alright. It’s sad what happened to him.”,
   
 “Ray Ray and I had a brief conversation about business. I asked him if he had any tips, he jokingly said ‘Just knock out the person at the top.’ I thought that was weird.”,
    “
  My mother has always been an impatient person that always wanted her way. I wouldn’t be surprised if she was getting him out of the way early.”]
  , 
     
  "Maid": [
 
 “I’d just finished cleaning the kitchen and went up the back steps. I was making my way to the third bathroom where I passed Connor in the hallway. While I was cleaning the bathroom I saw something out of the corner of my eye from the window facing the pool. I walked closer to get a better look when I realized something huge was floating in the pool. I rushed downstairs only to be horrified when I discovered it was Campaign Manager Lewis dead in the water.”,

   “He was such a great man, I'm going to miss seeing him as I work through the house and the smell of his cologne", 
   
   “If I can be completely honest...we were supposed to elope. The last thing we talked about were plane tickets.”, 
    
    “Connor and Ray Ray have been awkward with each other since he got here. There was never a time where I didn’t feel  tension in the room when they were together.”
]}





def mouseClicked():
    if mouseX >= 650 or mouseY <= 75:
        screenID=screenID+1
        
        
def mouseClicked():
    global POV
    if 80 <= mouseX <= 150 and 440 <= mouseY <= 510:
        POV["Shelby"][4] = POV["Shelby"][4]+1
    elif 360 <= mouseX <= 430 and 440 <= mouseY <= 510:
        POV["Connor"][4] = POV["Connor"][4]+1
    elif 640 <= mouseX <= 710 and 440 <= mouseY <= 510:
        POV["Maid"][4] = POV["Maid"][4]+1

