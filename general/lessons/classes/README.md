# Classes

## What are Classes?
>Classes are essentially a user-defined data type. Classes have a few components:

* Initializers
* Variables
* Methods

In order to better understand classes, we’ll look at it through a simple example. Imagine a class as a blueprint for a dog.

----
## Class Variables
In order to make our dog with our blueprint, we’ll need to start off by knowing different characteristics of the dog, like fur color, eye color, and age. These attributes can be stored as variables, and are called class variables. 

    	class Dog: 
    	#This line signifies that we are going to start defining a class called Dog
    	fur_color = "golden" #These lines are where Class Variables are defined.
    	eye_color = "blue"    
    	age = 3

----
## Instances

Now that we have a class (although it is a bit basic right now), we can initialize it.
Think of this as making your dog!
The syntax to initialize a class is as follows:

    	my_dog = Dog()
                   
Think of this as defining a variable called  my_dog, which is an instance of the class Dog

Now that we have our instance, what can we do with it?
For starters, let’s see if we can print our dog’s age! The code to do this would look like this:

    	print my_dog.age

If we want to change our dog’s age, or other characteristic, we would use the following code:

    	my_dog.age = 4

---
# Initializer

Yay! We have a dog. But there’s one problem with our dog: it doesn’t have a name.
You could say “oh, let’s just make another class variable for that”
But it’s not that simple! After all, then all our dogs would start out with the same name!
In order to specify a class variable when we initialize it, we need to create an Initializer function for that class.


The syntax for creating a class with an initializer is as follows:

    	class Dog:
    	fur_color = "golden" #Class variables (always the same, shared by all instances)
    	eye_color = "blue"
    	age = 3

    	def __init__(self, name): #Initializer (these variables are unique to each instance of the class)
    """the self parameter means that the function concerns other elements of the class, and the name parameter is the user input for what the dog’s name should be"""
    	self.name = name       

    	my_dog = Dog("Margy")
---
#  Methods

Congrats! You made it this far, but our dog’s not done yet, it needs to walk!
In order to make our dog be able to walk, the first step would be to have an instance variable for location, but muting this variable will be really clunky if we write a function outside the class.
This brings us to the next new concept, Class Methods.
Class methods are functions that are part of the class and change things inside the class.
In the next side, I’ll present some example code to show you how to make a method to make your dog walk!

    class Dog:
    	fur_color = "golden"  #Class variables (always the same, shared by all instances)
    	eye_color = "blue"
    	age = 3

    	def __init__(self, name, pos): #Initializer (these variables are unique to each instance of the class)
    	self.name = name     
    	self.pos = pos           

    	def walk(self, dist): #Class method (functions inside the class Dog that change the variable pos)
    	self.pos += dist   

    	my_dog = Dog("Margret", 0)
    	my_dog.walk(5)
    	print my_dog.pos #Returns 5
---
# Subclasses

What if we wanted to make different breeds of dog?
For example, say we wanted to make a dalmatian class.
In order to do this, we have two options:
* Create a whole new class from scratch
* Create a class based on the Dog() class and change the elements to fit a dalmatian

As you might have guessed, the second method is much more desirable, and there’s even a word for it: Subclasses
Next, you will learn how the syntax to create a subclass.
    	class Dog: #Parent Dog class
    	fur_color = "golden"
    	eye_color = "blue"
    	age = 3

    	def __init__(self, name, pos):
    	self.name = name     
    	self.pos = pos           

    	def walk(self, dist):
    	pos += dist   

    	class Dalmatian(Dog): #Child class of Dog
    	fur_color = "spotted"
    	eye_color = "black" #Only unique elements need to be specified

    	my_dalmatian = Dalmation("Fido", 1)
    	print my_dalmatian.age #The child inherits the age variable from the parent class
    	my_dalmatian.walk(3) #The child inherits the walk method from the parent class as well!
    	print my_dalmatian.pos #Returns 4
