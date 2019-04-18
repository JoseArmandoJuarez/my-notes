## Scripting with raw input

* Use the built-in function input
	
	    name = input(“Enter your name: ”)
	    print(“hello there, {}!”.format(name.title()))

* If want to use numbers (integers)
		
		num = int(input(“Enter integer: ”))
        print(num)

* Or want to use decimal numbers (float)
	
        num = float(input(“Enter number: ”))
        print(num)

* Adding both integer and float

	    num = int(float(input(“Enter a number: “)))
	    print(num)

* eval is a built-in function that evaluates a string as a line of python
* The eval() function evaluates the specified expression, if the expression is a legal Python statement, it will be executed.
		
		x = eval(input(“Enter an expression: ”))
		print(n)

---

* valueError -  problem with the content of the object you tried to assign the value to.
* Assertion Error - An assert statement fails something that shouldn't happen has happened.
* Index Error - A sequence subscript is out of range
* Key Error - A key that cannot be found in the dictionary
* Type Error - An object of an unsupported type is passed as input to an operation or function

---

* Opening files and reading

        f = open(‘my_path/my_file.txt’, ‘r’)  # r is only for reading not for writing
        file_data = f.read()
        f.close()

* Writing to a file

        f = open(‘my_path/my_file.txt’, ‘w’) 
        f.write(“Hello there!”)
        f.close()

* If file does not exist python will create it for you
* If opening a existing file and add content to it python will delete it and replace it with the new text/content. If you don't want that to happen use (‘a’)
* If you don't want to use close() use the following syntax
	
	    open(‘another_file.txt’. ‘r’) as f:
		file_data = f.read()

---

## Importing local scripts
* use the following:
	
        import nameOfScript

* to access objects from an imported module, you need to use dot notation.

        script_num.py
        num = 5 + 4

        script_display.py
        
        import script_num
        print(script_num.num)

* instead of using the file name all the time do this…

        import script_display as sd # sd becomes short for script_display
        print(sd.num)

1. To import an individual function or class from a module
    
        from mosule_name import object_name

2. To import multiple individuals objects from a module …
        
        from module_name import first_object, second_object

3. To rename a module

        import module_name as new_name 

4. To import an object from a module and rename it…
	
        from module_name import object_name as new_name

5. To import every object individually from a module (DO NOT DO THIS)

	    from module_name import *
	
	* Instead use ….

	        import module_name

---

## To install libraries use pip
* Example to install the time zone package

	    pip install package_name

* To install all requirements at once use…
	    
        pip install -r requirements.txt

