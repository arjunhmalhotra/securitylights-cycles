def main():
    #get input values from the user
    t1_on = int(input("Length of time first security light stays on: "))
    t1_off = int(input("Length of time first security light stays off: "))
    t2_on = int(input("Length of time second security light stays on: "))
    t2_off = int(input("Length of time second security light stays off: "))
    t_mailman = int(input("Time in minutes after midnight the mailman arrives: "))

    first = checkTimes(t1_on, t1_off, t_mailman)
    second = checkTimes(t2_on, t2_off, t_mailman)

    #print the answers
    if first and second == True:
        print("BOTH")
    elif first == True or second == True:
        print("ONE")
    else:
        print("NONE")


def checkTimes(t_on, t_off, t_mailman):
    """
    checkTimes(t_on, t_off, t_mailman)
    Parameters:
        t_on: the length of time that the light stays on
        t_off: the length of time that the light stays off
        t_mailman: the time that the mailman arrives
    Return values: a True or False value, depending on whether the mailman arrived
    while the light was on (True) or off (False)
    This function checks whether the light is on or off when the mailman arrives
    and returns a Boolean value with the answer.
    """
    currentTime = 0
    if t_mailman == 0:
        return True
    else:
        while currentTime <= 1440:
            currentTime += t_on
            if t_mailman < currentTime:     #if mailman arrives while the light is on
                return True
            elif t_mailman == currentTime:  #if mailman arrives as light turns off
                return False
            currentTime += t_off
            if t_mailman < currentTime:     #if mailman arrives while light is off
                return False
            elif t_mailman == currentTime:  #if mailman arrives as light turns on
                return True
        return False

main()
