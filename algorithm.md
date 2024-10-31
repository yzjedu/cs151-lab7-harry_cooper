Purpose: Calculate the cost based on the input of width, length, and floor type   
Name: calculate_room_cost     
Parameters:  width, length, flooring_type     
Algorithm: 
1) Based on the input of the floor type set the correct cost corresponding to the floor type   
2) calculate the area room by multiplying the width and length   
3) multiply the area by the cost of the floor type    
4) return the cost    

Purpose: check if the input of width or length is a real number   
Name: check_float
Parameters: val
Algorithm: 
1) check if the input value is a real number 
2) if the input value is above 0 
   1) return value
3) Otherwise return -999 

Purpose: Determine user package type  
Name: main   
Parameters: none   
Algorithm:
1) create variables for a loop and total price and set them to 0
2) when x is less than 5
   1) room number is one greater than x 
   2) Prompt the user to input the width of the room 
   3) When the width is not a decimal or whole number and is below 0 
      1) Prompt the user to input a valid input for the width 
   4) Prompt the user to input the length of the room 
   5) When the length is not a decimal or whole number and is below 0 
      1) Prompt the user to input a valid input for the length
   6) Prompt the user to input a floor type
   7) Calculate the pricing of the area based on floor type 
   8) Output the price for the room 
   9) Add the price of the room to the total cost
   10) dd 1 to x
3) Output the total price of the house