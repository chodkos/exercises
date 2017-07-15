-- nbFloors: number of floors
-- width: width of the area
-- nbRounds: maximum number of rounds
-- exitFloor: floor on which the exit is found
-- exitPos: position of the exit on its floor
-- nbTotalClones: number of generated clones
-- nbAdditionalElevators: ignore (always zero)
-- nbElevators: number of elevators
next_token = string.gmatch(io.read(), "[^%s]+")
nbFloors = tonumber(next_token())
width = tonumber(next_token())
nbRounds = tonumber(next_token())
exitFloor = tonumber(next_token())
exitPos = tonumber(next_token())
nbTotalClones = tonumber(next_token())
nbAdditionalElevators = tonumber(next_token())
nbElevators = tonumber(next_token())
elevatorsPosition = {}

for i=0,nbElevators-1 do
    -- elevatorFloor: floor on which this elevator is found
    -- elevatorPos: position of the elevator on its floor
    next_token = string.gmatch(io.read(), "[^%s]+")
    elevatorFloor = tonumber(next_token())
    elevatorPos = tonumber(next_token())
    elevatorsPosition[elevatorFloor] = elevatorPos
end

-- game loop
while true do
    -- cloneFloor: floor of the leading clone
    -- clonePos: position of the leading clone on its floor
    -- direction: direction of the leading clone: LEFT or RIGHT
    next_token = string.gmatch(io.read(), "[^%s]+")
    cloneFloor = tonumber(next_token())
    clonePos = tonumber(next_token())
    direction = next_token()
     
    if(cloneFloor == -1) then print('WAIT') 
    elseif cloneFloor == exitFloor then
       
            if (exitPos < clonePos) and (direction =='RIGHT') 
                or (exitPos > clonePos) and (direction =='LEFT') 
            then
                print('BLOCK')
            else
                print("WAIT") 
            end
    elseif (elevatorsPosition[cloneFloor] < clonePos and direction =='RIGHT')
        or (elevatorsPosition[cloneFloor] > clonePos and direction =='LEFT')
        then print('BLOCK')
    else print('WAIT')
    end
        
    
end
