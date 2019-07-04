# Murder-Mystery-Story

def setup():
    size(800,533)
    global screenID
    screenID = 0
    global question
    question = 0
    global i
    i = 0
    global current
    current=0
    global choice
    choice=""
def draw():
    global screenID
    #global question
    if screenID==0:
        startscreen()
    elif screenID==1:
        backgroundstory()
    elif screenID==2:
        qna()
    elif screenID==3 and i < 4:
        updateInfo()
        
    checkgamestatus()
    

    
def startscreen():
    img2 = loadImage("RealNext.png")
    size(800,533)
    img = loadImage ("House.jpg") 
    background(img) 
    textSize(30) 
    fill(255,255,255) 
    text("CSSI Murder Mystery",250,50) 
    fill(0) 
    rect(250,460,300,50) 
    textSize(30) 
    fill(255,255,255) 
    text("Click Next to begin", 260,465,350,50)
    image(img2,650,0,150,75)
    
def backgroundstory():
    img=loadImage("aqua_nueva_El_Salon_private_dining_room.jpg")
    img2=loadImage("RealNext.png")
    background(img)
    fill(255,255,255)
    textSize(30)
    text("Background Story",300,50)
    textSize(20)
    fill(0,0,0)
    rect(0,325,800,190)
    fill(255,255,255)
    text("Mayor Shelby Owens finally passed her new gun reform bill, to celebrate she \n decided to have a banquet at her mansion. After a night full of fun, the guests \n left, leaving the Mayor, live-in maid, the Mayor's son, Connor, and Mayor Owens' \n campaign manager, Ray Ray Lewis. They were all planning on spending the \n night until something horrific happened. Ray Ray was found floating face down \n in the pool.",10,350)
    image(img2,650,0,150,75)
    
def verdictScreen():
    img2=loadImage("RealNext.png") 
    office = loadImage("office2.jpg") #the image is on my desktop
    size(800,533)
    image(office,0,0,800,533)
    textSize(25)
    textAlign(CENTER)
    #fill(0,0,0)
    #rect(0,175,800,225)
    fill(255,255,255)
    text("Correct. \n The Killer is the Maid. Ray Ray and the maid had a sexual \n relationship for a long time. However, she found out the Mayor \n and Ray Ray had the same relationship. The maid was deeply in \n love with Ray Ray, yet he didn't feel the same way, causing \n her to take the knife from the kitchen and kill him.",400,200) 
    image(img2,650,0,150,75)
    
def updateInfo():
    global i
    fill(0,0,0)
    rect(0,60,800,325)
    fill(255,255,255)
    textSize(15)
    textAlign(CENTER)
    text(POV["Shelby"][i],400,130)
    #400
    textSize(20)
    textAlign(CENTER)
    text(POV["questions"][i], 400,90)
    textSize(15)
    textAlign(CENTER)
    text(POV["Connor"][i],370,220)
    #370
    textSize(15)
    textAlign(CENTER)
    text(POV["Maid"][i],370,310)
    #370
    
    
    stroke(255,255,255)
    fill(255,0,0)
    rect(740,180,40,40)
    
    fill(0,0,0)
    
    textSize(20)
    textAlign(CENTER)
    text(POV["Shelby"][4],760,210)
    
    stroke(255,255,255)
    fill(0,255,0)
    rect(740,240,40,40)
    
    fill(0,0,0)
    
    textSize(20)
    textAlign(CENTER)
    text(POV["Connor"][4],760,270)
    
    stroke(255,255,255)
    fill(0,0,255)
    rect(740,300,40,40)
    
    fill(0,0,0)
    
    textSize(20)
    textAlign(CENTER)
    text(POV["Maid"][4],760,330)
    
def checkgamestatus():
    if i == 4:
        if POV["Maid"][4] >= 2:
            verdictScreen()
        else:
            gameOver()
        
    

 #code for questions and answers screen
def qna():
    img2 = loadImage("RealNext.png") 
    size(800,533)
    background(0,0,0)
    name = "CSSI Murder Mystery" 
    background(0)
    textSize(40)
    textAlign(CENTER)
    text("CSSI Murder Mystery",400,50)
    
    textSize(20)
    textAlign(CENTER)
    text(POV["questions"][i], 400,90)
    
    textSize(15)
    textAlign(CENTER)
    text(POV["Shelby"][i],400,130)
    
    textSize(15)
    textAlign(CENTER)
    text(POV["Connor"][i],370,220)
    
    textSize(15)
    textAlign(CENTER)
    text(POV["Maid"][i],370,310)
    
    textSize(25)
    textAlign(CENTER)
    text("Who do you suspect the most?", 400, 425)
    
    stroke(255,255,255)
    fill(255,0,0)
    rect(740,180,40,40)
    
    fill(0,0,0)
    
    textSize(20)
    textAlign(CENTER)
    text(POV["Shelby"][4],760,210)
    
    stroke(255,255,255)
    fill(0,255,0)
    rect(740,240,40,40)
    
    fill(0,0,0)
    
    textSize(20)
    textAlign(CENTER)
    text(POV["Connor"][4],760,270)
    
    stroke(255,255,255)
    fill(0,0,255)
    rect(740,300,40,40)
    
    fill(0,0,0)
    
    textSize(20)
    textAlign(CENTER)
    text(POV["Maid"][4],760,330)
    
    stroke(255,255,255)
    fill(255,0,0)
    rect(80,440,70,70)
    
    fill(255,255,255)
    textSize(19)
    textAlign(CENTER)
    text("Mayor",116,480)
    
    stroke(255,255,255)
    fill(0,255,0)
    rect(360,440,70,70)
    
    fill(255,255,255)
    textSize(18)
    textAlign(CENTER)
    text("Connor",395,480)
    
    
    stroke(255,255,255)
    fill(0,0,255)
    rect(640,440,70,70)
    
    fill(255,255,255)
    textSize(19)
    textAlign(CENTER)
    text("Maid",676,480)
    
    fill(255,255,255)
    image(img2,650,0,150,75)

   
def mouseClicked():
    global screenID
    global i
    if mouseX >= 650 and mouseY <= 75:
        if screenID != 3:
            screenID=screenID+1
        if screenID == 3:
            i=i+1
            print i
            
    global POV
    global current
    if current == i:
        global choice
        if choice == "":
            if 80 <= mouseX <= 150 and 440 <= mouseY <= 510:
                POV["Shelby"][4] = POV["Shelby"][4] +1
                choice = "Shelby"
            elif 360 <= mouseX <= 430 and 440 <= mouseY <= 510:
                POV["Connor"][4] = POV["Connor"][4] +1
                choice = "Connor"
            elif 640 <= mouseX <= 710 and 440 <= mouseY <= 510:
                POV["Maid"][4] = POV["Maid"][4] +1
                choice = "Maid"
        else:
            if choice != "Shelby" and 80 <= mouseX <= 150 and 440 <= mouseY <= 510:
                POV[choice][4] = POV[choice][4] -1
                POV["Shelby"][4] = POV["Shelby"][4] +1
                choice = "Shelby"
            elif choice != "Connor" and 360 <= mouseX <= 430 and 440 <= mouseY <= 510:
                POV[choice][4] = POV[choice][4] -1 
                POV["Connor"][4] = POV["Connor"][4] +1
                choice = "Connor"
            elif choice != "Maid" and 640 <= mouseX <= 710 and 440 <= mouseY <= 510:
                POV[choice][4] = POV[choice][4] -1 
                POV["Maid"][4] = POV["Maid"][4] +1 
                choice = "Maid"
                
    else:
        current = i
        choice = ""



        
def gameOver():
    background(90,8,8)
    size(800,533)
    textAlign(CENTER)
    textSize(70)
    fill(255,255,255)
    text("GAME OVER",400,230)

    textAlign(CENTER)
    textSize(30)
    text("You have chosen the wrong suspect",400,330)
        

POV = {"questions":["Where were you between 1:30 - 2:30 am on Saturday morning?", "What was your relationship with the victim?", "What was the last conversation you had with the victim?", "Who do you suspect?"],
    "Shelby":["Mayor Owens: My campaign manager, my son and I were talking on the couch about the banquet\n when Connor you know my son Connor, went to the bathroom. Right after Ray Ray said he went to his car\n and I went to my office. It was maybe 10 minutes later when I heard the maid scream.","Mayor Owens: He was exactly what the title suggested, my campaign manager, nothing more, nothing less.", "Mayor Owens: Our last private conversation had a lot to do with the future. Things such as re-election and if \n I'd ever run for a higher position in office. I told him let's start off small, but he insisted. When I \n declined, he asked for a raise, so I cut the conversation short.", "Mayor Owens: The Maid because I would always find her and Ray Ray in compromising situations; they \n seemed fairly comfortable with each other.",0],
    "Connor":["Connor: My mom, Ray Ray and I were chilling on the couch.  When I got up to go make a call \nin my room. After the call I was making my way back to the drawing room and got halfway down \n the stairs when I heard a scream.","Connor: I didn't know much about him, seemed like a cool guy. He even hand delivered my \n invitation to me, so clearly he was alright. It's sad what happened to him.","Connor: Ray Ray and I had a brief conversation about business. I asked him if he had any tips, he \n jokingly said 'Just knock out the person at the top.' I thought that was weird.","Connor: My mother has always been an impatient person that always wanted her way. I wouldn't \n be surprised if she was getting him out of the way early.",0], 
    "Maid":["Maid: I'd just finished cleaning the kitchen and went up the back steps. I was making my way to the\n third bathroom where I passed Connor in the hallway. While cleaning the bathroom I saw something\n out of the corner of my eye from the window facing the pool, I was horrified. I rushed downstairs and \n discovered it was Campaign Manager Lewis dead in the water.","Maid: He was such a great man, I'm going to miss seeing him as I work through the house and the \n smell of his cologne","Maid: If I can be completely honest...we were supposed to elope. The last thing we talked about were \n plane tickets.","Maid: Connor and Ray Ray have been awkward with each other since he got here. There was never a \n time where I didn't feel tension in the room when they were together.",0]}


        
    
#POV["Shelby"][0]
