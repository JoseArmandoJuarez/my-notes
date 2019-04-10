
## Arrays

* Note: use double quotes “” not single ‘’

    list_of_random = [1, 2, 3, 4, 5, “a string”, True]

* To check the index

    print(list_of_random[1]) 
    
    #output - 2

* To check how many elements/length

    * DO NOT:
    
        list_of_random[len(list_of_random)]

    * DO, instead retrieve the last element by reducing the index by 1

        list_of_random[len(list_of_random) -1]

---

## Slicing

    week_days = [“Monday”, ”Thursday”, “Wednesday”, “Tuesday”, “Friday”, “Saturday”, “Sunday”]
    week_days [3:6]
    #Start at 3 and end at 6
    #output - ‘Tuesday’, ‘Saturday’, ‘Sunday’

---

## Are you IN or  NOT IN (returns a bool)

    print(‘this’ in ‘this is a string’)
    #output - True

    print(‘in’ in ‘this is a string’)
    #output - True 
    #(string - “str ‘in’ g”)

	print(5 not in [1, 2, 3, 4, 6])
	#output - True

    print(5 in [1, 2, 3, 4, 6])
	#output - False

---

## MUTABILITY
* Mutability is about whether or not we can change an object once it has been created. If an object like a list or string can be changed like a list can, then it is called mutable. However, if an object cannot be changed with creating a completely new object like a string, then the object is considered immutable.
* As shown below you are able to replace 1 with ‘one’. This is because lists are mutable.


        my_list = [1, 2, 3, 4, 5]
        my_list [0] = ‘one’
        print(my_list)

        #output - [‘one’, 2, 3, 4, 5]

---

## .max() Method

* Returns the greatest element of the list

        letters = [“A”, “C”, “G”, “X”, “R”, “D”]
        print(max(letters))
        # output - X

---

## .min() Method
* Returns the smallest element of the list.

        numbers = [3, 42, 5, 6, 1, 63, 46, 73]
        print(min(numbers))
        # output - 1

---

## .sorted() Method
* Returns a copy of a list in order from smallest to largest, leaving the list unchanged

        sizes = [15, 6, 89, 34, 65, 35]
        print(sorted(sizes))
        #output - [6, 15, 24, 35, 65, 89]

* Another way:

        print(sorted(sizes, reverse = True))
        #output - [89, 65, 35, 24, 15, 6]

---

## .join() Method

    name = “-”.join([“Garcia”, “O’kelly”])
    print(name)
    #output - Garcia-O’kelly

    new_str = “\n”.join([“A”, “B”, “C”, “D”])
    print(new_str)
    #output - A
	   B
 	   C
	   D

---

## .append() Method
* Is able to add another item to the list

        letters = [“a”, “b”, “c”, “d”]
        letters.append(“z”)
        print(letters)
        #output [“a”, “b”, “c”,” d”, “z”]

---

## Tuples
* A tuple is a collection which is ordered and unchangeable. In Python tuples are written with round brackets. You can’t remove or add items from tuples or sort them in place.

        thistupe = (“apple”, “banana”, “cherry”)
        print(thistuple[1])
        #output - banana

* Try to replace banana to orange. Well you can’t

        thistupe = (“apple”, “banana”, “cherry”)
        Thistuple[1] = orange
        #output - apple, banana, cherry

---

## .set() Method
* Removes duplicates

        countries = [“Angola”, “Maldives”, “India”, “United States”, “India”, “Denmark”, “Angola”]

        country_set = set(countries)
        print(country_set)
        #output - {“Angola”, “Maldives”, “India”, “United States”, “Denmark”}

* To remove or add an element use the .add() and .pop() method

        fruit = {“apple”, “banana”, “orange”, “grapefruit”}
        print(“watermelon” in fruit)
        #output - False


    * .add method (in this case it adds it randomly)

            fruit.add(“watermelon”)
            print(fruit)
            #output - fruit = {“grapefruit”, “apple”, “banana”, “watermelon”,“orange”}

    * .pop() method (In this case it removes a random fruit)

            print(fruit.pop())
            print(fruit)
            #output - fruit = {“grapefruit”, “banana”, “watermelon”,“orange”}

---

## Dictionaries And Identity Operators
* A dictionary is a mutable data type that stores mappings of unique keys to values.

        elements = {“hydrogen”: 1, “helium”: 2, “carbon”: 6}
        # A Dictionary has a key and a value 
        # hydrogen = key
        # 1 = value

* Can also add more values like this

        elements = {“hydrogen”: 1, “helium”: 2, “carbon”: [1, 2, 3]}

        #Insert a new key with a value of 3
        Elements[“lithium”] = 3

---

## Compound data Structures
* Can include containers in other containers to create compound data structures.

        elements = { “hydrogen”: { “number”: 1
                                    “weight”: 1.00794,
                                    “symbol”: “H” 
                                },
                                { “number”: 2,
                                    “weight”: 4.002602,
                                    “symbol”: “He” 
                                } 
                    }

* Can access elements in this nested dictionary like this...

        helium = elements[“helium”] #get the helium dictionary
        Hydrogen_weight = elements[“hydrogen”][“weight”] #get the hidrogen weight


* You can also add a new key to the element dictionary.

        oxygen = {“number”: 8, “weight”: 15.999, “symbol”: “O”} #create new dictionary

        elements = [“oxygen”] = oxygen 
        #assign ‘oxygen’ as a key to the elements dictionary

        print(‘elements = ’, elements)

        #output
        elements = { “hydrogen”: { “number”: 1
                                    “weight”: 1.00794,
                                    “symbol”: “H” 
                                },
                                { “number”: 2,
                                    “weight” 4.002602,
                                    “symbol”: “He” 
                                },
                                { “number”: 8,
                                    “weight”: 15.999,
                                    “symbol”: “O” 
                                }
                    }
