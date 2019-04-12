## Functions

    def cylinder_volume(height, radius):

	    pi = 3.14159
	    volume = height * pi * radius * 2
	    return volume

    cylinder_volume(10, 3)


## Defining a function
* Header
    * Always start with the def keyword meaning that this is a function
    * Then the name of the function
    * In the parentheses, may include arguments separated by commas
    * The parameters hold a value such as height = 10 and radius = 3
    * And it always ends with a colon (:)
* Body
    * This is where the function does it's work
    * This function does a small calculation volume = height * pi * radius * 2
    * The body sometimes includes a return statement which returns back an output value to the called function which is cylinder_volume(10, 3)

## Passing arguments

	cylinder_volume (10, 7)  #by position
	cylinder_volume (height = 10, radius = 7) #by name


Example:
* Turn the amount of days into weeks and count the remaining.

        def readable_timedelta(days):
            
            days_in_week = days // 7
            days_left = days % 7
            return “{} week(s) and {} day(s)”.format(days_in_weeks, days_left)

        print(readable_timedelta(10))

        #output 
        1 week(s) and 3 day(s)

---

## Variable scope

* Variable scope refers to which parts of a program a variable can be referenced or used from.

* If a variable is created inside a function, it can only be used within that function. Accessing it outside that function is not possible.

---

## Lambda Expressions

* Use lambda expressions to create anonymous functions. (functions that don't have a name)

        def multiply(x, y):
            
            return x * y

        multiply(4, 7)

        #output -  28

* This can be reduced to...

        multiply = lambda x, y : x * y
        multiply(4, 7)
        
        #output -  28


