# -第7組
組員名單:  機一B  0614127  楊智傑 機一A 0614018 曹鈞崴 機一B 0614151 汪祐安 營建4B 0312090 戴于凱 營建4B 0312092 陳伯任
主題:汲汲營營
工作分配:機一B  0614127  楊智傑 資料查詢 
機一A 0614018 曹鈞崴 資料查詢 
機一B 0614151 汪祐安 簡報製作 
營建4B 0312090 戴于凱 輸入程式
營建4B 0312092 陳伯任 輸入程式
程式碼
local bg = display.newImage ("nkfust.jpg") 
bg.x = display.contentCenterX
bg.y = display.contentCenterY 
出現圖檔，並且定位它的位置
local floor=display.newRect(0,0,800,300)
floor.x = 0
floor.y = 620
floor:setFillColor(0, 0, 0)
地位地板長度、寬度、位置、顏色
local balloon=display.newImage("ballon.png",display.contentCenterX,display.comtentCenterY)
balloon.x=150
定位圖檔的位置
local physics=require("physics")
physics.start()
physics.addBody(balloon,{bounce=0})
physics.addBody(floor,"static")
local function push()
    balloon:applyLinearImpulse(0,-2,balloon.x,balloon.y)
  end
  
balloon:addEventListener("tap",push)
設定物理性質，球的彈性，點下去會上彈的性質

