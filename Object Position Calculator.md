# Object Position Calculator
This is one of the first *Python* programs that I ever wrote. I am proud of this program because I learned so much while working on it. While the code is rather unorganized and unsightly it was the first time I used functions in Python effectively. This helped me gain a deeper understanding of Python and object orientated programing in general

    def main(): 
    while True:
        finalpost = solve()
        print("The object's final position is ",finalpost)
        print("Would you like to continue?")
        print("Enter 'y' to continue. Enter anything else to quit")
        endit = input()
        if endit != "y":
            break
	def findxint():
    while True:
        try:
            xint = float(input("What is the object's inital position?: "))
        except ValueError:
            print("You must enter a number!")
        else:
            break
    return xint                  
	def findvint():
    while True:
        try:
            vint = float(input("What is the object's inital velocity?: "))
        except ValueError:
            print("You must enter a number!")
        else:
            break
    return vint                  
	def findacc():
    while True:
        try:
            acc = float(input("What is the object's accerlation?: "))
        except ValueError:
            print("You must enter a number!")
        else:
            break
    return acc             
	def findtime():
    while True:
        try:
            time = float(input("Time elapsed: "))
            if time < 0:
                raise ValueError
        except ValueError:
            print("Time must be entered as a number greater than or equal to zero!")
        else:
            break
    return time     
	def solve():
    xint = findxint()
    vint = findvint()
    acc = findacc()
    time = findtime()
    finalpost = (xint) + (vint*time) + (0.5*acc*time**2)
    return finalpost
	main()



[Return to Home](https://github.com/CalvinNanneman/INFOTC-1000-Final/blob/main/README.md#welcome-to-calvins-infotc-1000-final-project)
