count = 1
goes_up = 0
times = 0
highest_streak = 0


function is_valid_number(input_str)
    local num_value = tonumber(input_str)
    if num_value == nil then
        return false
    elseif math.type(num_value) ~= "integer" then
        return false
    elseif num_value <= 0 then
        return false
    else
        return true
    end
end


print("Welcome to the 3n + 1 machine\n")


while true do
    io.write("Type your number: ")
    local nhap = io.read()  


    if is_valid_number(nhap) then
        number_value = tonumber(nhap)
        break
    else
        print("Invalid input. Please type a valid whole positive number\n")
    end
end


while true do
    print(number_value)
    if number_value == 1 then
        print("The number goes to 1")
        print(string.format("\nThe steps for the number to 1 is: %s", count))
        print(string.format("\nThe amount of the number going up is: %s", goes_up))
        print(string.format("\nThe longest streak going up of the number is: %s", highest_streak))
        break
    elseif (number_value % 2) == 0 then
        number_value = number_value / 2
        print(number_value)
        count = count + 1
        goes_up = goes_up + 1
        times = times + 1
        if times > 3 then
            streak = times
        end
    else
        number_value = (number_value * 3) + 1
        print(number_value)
        count = count + 1
        if times > 3 then
            if times > highest_streak then
                highest_streak = times
            end
        end
        times  = 0
    end
end
