def find_second_highest(nums):
    if len(nums) < 2:
        return None 
    
    highest = float('-inf')
    second_highest = float('-inf')
    
    for num in nums:
        if num > highest:
            second_highest = highest
            highest = num
        elif num > second_highest and num < highest:
            second_highest = num
    
    if second_highest == float('-inf'):
        return None  
    
    return second_highest

input_list = [1, 4, 7, 8, 4, 8, 1, 4, 9]
print(find_second_highest(input_list))  
