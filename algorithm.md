def calculate_room_cost(width, length, flooring_type):
    # Cost per square foot for each flooring type
    if flooring_type == 'hardwood':
        flooring_cost = 1.39
    elif flooring_type == 'carpet':
        flooring_cost = 3.99
    elif flooring_type == 'tile':
        flooring_cost = 4.99
    
    # Calculate area and cost for the room
    area = width * length
    cost = area * flooring_cost 
    
    return cost
    
# Determine if the input of width or length is a float/ number 
def check_float(val):
    num_check = val.replace('.','',1)
    if num_check.isdigit():
        val = float(val)
        if val > 0:
            return val
        else:
            val = -999
            return val
    else:
        val = -999
        return val
    
        
    

def main():
    # Output an introduction
    print('Welcome to the Flooring Cost Calculator!')
    
    # Create variables needed
    x = 0
    total_price = 0
    
    # Create a loop to loop five times 
    while x < 5:
        room_number = x + 1
        # ask user to input width
        width = input(f'Enter the width for room {room_number} (in feet):')
        while check_float(width) == -999:
            width = input(f'Enter the width for room {room_number} (in feet):')
        width = float(width)
        
        # ask user to input length
        length = input(f'Enter the length for room {room_number} (in feet):')
        while check_float(length) == -999:
            length = input(f'Enter the length {room_number} (in feet):')
        length = float(length)
        # ask user to input flooring type
        flooring_type = input('Enter the flooring type (hardwood, carpet, tile): ').lower()
        while flooring_type != 'hardwood' and flooring_type != 'carpet' and flooring_type != 'tile':
            flooring_type = input("Enter the flooring type (hardwood, carpet, tile): ").lower()
        # calculate and output room cost
        room_cost = calculate_room_cost(width, length, flooring_type)
        print(f'Cost for Room {room_number} with {flooring_type} flooring costs: ${room_cost:.2f}')
        # add room cost to the total
        total_price += room_cost
        x += 1
    # output price of the total flooring for the house  
    print(f'total cost for the flooring of the house is ${total_price:.2f}')
    print('Thank you for using the Flooring Cost Calculator!')
# run main
main()
    
