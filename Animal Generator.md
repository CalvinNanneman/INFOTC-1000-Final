# Animal Generator
This is another one of my Python projects. This project helped me understand the concept of classes and objects in Python. This was a new experience using Python built in modules as well as a custom module.

**Code for my Animal module**

    
	class Animal:
    def __init__(self, __animal_type, __name, __mood):      #attributes for animals
        self.get_animal_type = __animal_type
        self.get_name = __name                              #methods to get attributes for a given animal object
        self.check_mood = __mood

    def print_animal_list(self):                            #print method to be used to display all attributes for animal objects
        print(self.get_name, "the", self.get_animal_type, "is", self.check_mood)





**Code for the Animal Generator**

    
	import random             #import random module for use in the mood gene
	from Animal import Animal #import module for the animal class
	
	def main():                      #main function calls userinput to get the list of animals then prints the list
    animalList = userinput()
    print("\nAnimal List:") 
    for x in animalList:
        x.print_animal_list()    #using the print method from the class animal

	def findmood():                  #function that randomly generates a 'mood' then returns that value
    mood = random.randint(1,3)
    if mood == 1:
        mood = 'Happy'
    if mood  == 2:
        mood = 'Hungry'
    if mood == 3:
        mood = 'Sleepy'
    return mood

	def userinput():     #function to gather user input, create animal objects and add them to a list
    moreinput = True
    animalList = []  #initiating a list for our animal objects
    while moreinput:
        mood = findmood() #the mood function needs to be called inside the loop for mood to be random for each animal
        animaltype = (input("What is the animal type?: ")) 
        animalname = (input("What is the animal's name?: "))
        animal_temp = Animal(animaltype, animalname, mood)    #temporary variable to create animal Object before passing to list
        animalList.append(animal_temp)

        nomoreinput = input("\nWould you like to make another animal? y/n: ") 
        if nomoreinput != 'y':
            moreinput = False
    return animalList

	main()


[Return to Home](https://github.com/CalvinNanneman/INFOTC-1000-Final/blob/main/README.md#welcome-to-calvins-infotc-1000-final-project)
