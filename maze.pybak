# maze program by Katelyn Winter
setMediaPath('/Users/PC3/Documents/gitHub/maze')
class Maze(object):
  """ solves a maze """
  def __init__(self):
    self.image = makePicture('maze.jpg')
    self.w = makeWorld(getWidth(self.image),getHeight(self.image))
    self.w.setPicture(self.image)
    self.t = makeTurtle(self.w)

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
    
    
    
    
    
    
    