
## If, elif, else
	
    season = 'spring'

	If season == ‘spring’:
		print(‘Plant the garden!’)
	elif season == ‘summer’:
		print(‘Water the garden!’)
	else:
		print(‘Unrecognized season’)
    
    #output - Plant the garden!

* if the season is spring it enters the first statement and prints out 'Plant the garden!'
* else if the season is equal to summer the statement prints out 'Water the garden!'
* else if the season is equal to none of the statements then 'Unrecognized season'

---

## for loops

	cities = [“new york city”, “mountain view”, “chicago”, “los angeles”]

	# city-loops iteration variable
    # cities-iterable
	for city in cities:
		print(city.title())

	#output
		New York City
		Mountain View
		Chicago
		Los Angeles

---

## range() Function with for loops
* Repeats an action a certain number of times
	
        For i in range(3):
            print(“Hello!”)
        
        #output
            Hello!
            Hello!
            Hello!

* range(start, stop, step)
    * start - is the first number of the sequence if unspecified, defaults to 0
    * stop - is 1 more than the last number of the sequence. Must be specified
    * step - is the difference between each number in the sequence, if unspecified defaults to 1

* Examples:
	* range(4) - returns 0,1, 2, 3
	* range(2,6) - returns 2,3,4,5 (start at 2 end at 6)
    * range(1, 10, 2) - returns 1,3,5,7,9 (start at 1 end at 10 step every other 2 numbers)

---

## Counting words in a dictionary / for loop

    book_title = [“great”, “expectations”, “the”, “adventures”, “great”, “fin”]
    word_counter = {}

    for word in book_titles:
        if word not in word_counter:
            word_counter[word] = 1
    else:
            word_counter[word] += 1

    print(word_counter)
        
    #output
    {‘great’: 2, “expectations”: 1, “the”: 1, “adventures”: 1, “fin”: 1}

### What's happening here?
* The for loop iterates through each element in the list. For the first iteration, word takes the value 'great'.

* Next, the if statement checks if word is in the word_counter dictionary.

* Since it doesn't yet, the statement word_counter[word] = 1 adds great as a key to the dictionary with a value of 1.

* Then, it leaves the if else statement and moves on to the next iteration of the for loop. word now takes the value expectations and repeats the process.

* When the if condition is not met, it is because that word already exists in the word_counterdictionary, and the statement word_counter[word] = word_counter[word] + 1 increases the count of that word by 1.

* Once the for loop finishes iterating through the list, the for loop is complete.

---

Iterating through dictionaries with for loops
	
	cast = {
		“Jerry Seinfeld” : “Jerry Seinfeld”,
		“Julia Louis” : “Elaine Benes”,
		“Jason Alexander” : “George Costanza“,
		“Michael Richards” : “Cosmo Kramer”
    }

    for key in cast:
	    print(key) #only prints out the key

    #output
		Jerry Seinfeld
		Julia Louis
		Jason Alexander
		Michael Richards

* Print out both sides
		
	    for key, value in cast.items():
		    print(“Actor: {}   Role: {}”.format(key, value))

	    #output -
            Actor: Jerry Seinfeld   Role: Jerry Seinfeld”,
            Actor: Julia Louis   Role: Elaine Benes
            Actor: Jason Alexander   Role: George Costanza
            Actor: Michael Richards   Role: Cosmo Kramer

---

## Factorial using  a while loop

* Find factorial of 6
	    
        number = 6
	    product = 1
	
* Track the current number being multiplied
	
        current = 1
	
        while current <= number:
            product *= current        #1*1, 1*2, 1*3….
            current += 1
 
        print(product) #output 270

---

## Break & Continue
* Use break in a loop when you want to end the loop
* Use a continue to skip one iteration of a loop

* USING THE BREAK METHOD

        manifest = [("bananas", 15), ("mattresses", 24), ("dog kennels", 42), ("machine", 120), ("cheeses", 5)]

        # the code breaks the loop when weight exceeds or reaches the limit

        weight = 0
        items = []
        for cargo_name, cargo_weight in manifest:
            print("current weight: {}".format(weight))
            if weight >= 100:
                print("  breaking loop now!")
                break
            else:
                print("  adding {} ({})".format(cargo_name, cargo_weight))
                items.append(cargo_name)
                weight += cargo_weight

        print("\nFinal Weight: {}".format(weight))
        print("Final Items: {}".format(items))

        #output
            current weight: 0
            adding bananas (15)
            current weight: 15
            adding mattresses (24)
            current weight: 39
            adding dog kennels (42)
            current weight: 81
            adding machine (120)
            current weight: 201
            breaking loop now!

            Final Weight: 201
            Final Items: ['bananas', 'mattresses', 'dog kennels', 'machine']

* USING THE CONTINUE METHOD

        # skips an iteration when adding an item would exceed the limit
        # breaks the loop if weight is exactly the value of the limit

        weight = 0
        items = []
        for cargo_name, cargo_weight in manifest:
            print("current weight: {}".format(weight))
            if weight >= 100:
                print("  breaking from the loop now!")
                break
            elif weight + cargo_weight > 100:
                print("  skipping {} ({})".format(cargo_name, cargo_weight))
                continue
            else:
                print("  adding {} ({})".format(cargo_name, cargo_weight))
                items.append(cargo_name)
                weight += cargo_weight

        print("\nFinal Weight: {}".format(weight))
        print("Final Items: {}".format(items))

        #output
        current weight: 0
        adding bananas (15)
        current weight: 15
        adding mattresses (24)
        current weight: 39
        adding dog kennels (42)
        current weight: 81
        skipping machine (120)
        current weight: 81
        adding cheeses (5)

        Final Weight: 86
        Final Items: ['bananas', 'mattresses', 'dog kennels', 'cheeses']

---

## Zip method combine 2 into 1 list

	items = [“bananas”, “mattresses”, “dog kernels”, “machine”, “cheeses”]
	weights = [15, 34, 42, 120, 5]

1. This one way to do it…
    
        print(list(zip(items,weights)))
      
2. This another way…
	    
        for item, weight in zip(items, weights):
		    print(item, weight)

        #output- 
	        [(“bananas”, 15), (“mattresses”, 34), (“dog kernels”, 42), (“machine”, 120), (“cheeses”, 5)]

## Unzip a list

	items, weights = zip(*manifest)
    print(items)
    print(weights)

---

## Numbering List
	
	items = [“bananas”, “mattresses”, “dog kernels”, “machine”, “cheeses”]
	
	for i, item in zip(range(len(items)),items):
		print(i, item)
	
    #output
        0 bananas
    1 mattresses
    2 dog kernels
    3 machine
    4 cheeses

---

## List comprehensions
	
	capitalized_cities = []
	
	for city in cities:
		capitalized_cities.append(city.title())

* Can be reduced to...

        capitalized_cities = [city.title() for city in cities]

* This list comprehension above calls city.title() ]for each element city in cities, to create each element in the new list, capitalized_cities


