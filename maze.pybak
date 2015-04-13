# maze program by Katelyn Winter
setMediaPath('/Users/Katelyn/Documents/gitHub/maze')
class Maze(object):
  """ solves a maze """
  def __init__(self):
    self.image = makePicture('maze.jpg')
    self.w = makeWorld(getWidth(self.image),getHeight(self.image))
    self.w.setPicture(self.image)
    self.t = makeTurtle(self.w)
    penUp(self.t)
    moveTo(self.t,30,190)
    turnRight(self.t)
  def colorInFront(self):
    move = 11
    self.c = 'colorInFront()'
    x = getXPos(self.t)
    y = getYPos(self.t)
    h = self.t.getHeading()
    if h == 0:
      y = y - move
    if h == 90 or h == -270:
      x = x + move
    if h == 180 or h == -180:
      y = y + move
    if h == -90 or h == 270:
      x = x - move
        
    self.pos = getPixelAt(self.image,x,y)
    color = getColor(self.pos)
    if distance(color,white) < 150:
      return white
    if distance(color,blue) < 150:
      return blue
    if distance(color,green) < 150:
      return green
    if distance(color,red) < 150:
      return red
    if distance(color,yellow) < 150:
      return yellow
    return blue # must be a wall 
      
            

# Tests follow here
doTests = 1
if doTests:
  # Test no.1
  m = Maze()
  
  #Test no.2
  if m.image.__class__  == Picture:
    printNow("Test2 passed, Image exists.")
  else:
    printNow("Test2 failed, Image doesn't exist.")
  
  # Test no.3
  try:
    if m.w.__class__ == World:
      printNow("Test 3 passed, World exists.")
  except:
    printNow("Test 3 failed.")
    
  # Test no.4
  try:
    if m.w.getPicture().fileName[-8:] == 'maze.jpg':
      printNow("Test 4 passed, world picture is maze.jpg")
    else:
      printNow("Test 4 failed, world picture is " + m.w.getPicture().fileName)
  except:
    printNow("Test 4 failed, unable to get file name.")
  
  #Test no.5
  try:
    if m.t.__class__ == Turtle:
      printNow("Test 5 passed, Turtle exists.")
    else:
      printNow("Test 5 failed, Turtle does not exist.")
  except:
    printNow("Test 5 failed, class isn't a Turtle." + str(m.t.__class__)) 
  
  #Test no.6
  try:
    if m.t.getXPos() == 30:
      printNow("Test 6 passed, Turtle is at X start.")
    if m.t.getYPos() == 190:
      printNow("Test 6 passed, Turtle is at Y start.")
    else:
      printNow("Test 6 failed, Turtle is not at X and/or Y start.")
  except:
     printNow("Test 6 failed, could not get X or Y start." + str(m.t.getXPos()) + str(m.t.getYPos()))
     
  #Test no.7
  if dir(m).index('colorInFront') > 0:
    printNow("Test 7 passed, colorInFront exists.")
  else:
    printNow("Test 7 failed, colorInFront doesn't exist.")
 
    
  #Test no.8
  try:
    if m.colorInFront() == white:
      printNow("Test 8 passed, colorInFront is white.")
    else:
      drop(m.t)
      printNow("Test 8 failed, colorInFront isn't white.")
  except:
    printNow("Test 8 failed, couldn't get color.")
    
  #Test no.9
  turnLeft(m.t)
  turnLeft(m.t)
  if m.colorInFront() == blue:
    printNow("Test 9 passed, colorInFront is blue due to wall.")
  else:
    printNow("Test 9 failed, colorInFront isn't blue, doesn't see a wall.")
    
    
    
    
    