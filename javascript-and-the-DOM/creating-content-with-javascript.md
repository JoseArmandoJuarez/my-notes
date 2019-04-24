
## Updating existing page content

* .innerHTML property sets or returns the HTML content inside the selected element.
* .outerHTML represents the HTML element itself, as well as it's children

        Example: 

        <h1 id=”pick-me”>Greeting To <span>All</span>!</h1>

        var innerResults = document.querySelector(‘#pick-me’).innerHTML;
        console.log(innerResults);
        //logs the string: “Greetings To <span>All</span>!”

        var outerResutls = document.querySelector(‘#pick-me’).outerHTML;
        console.log(outerResults);
        //logs the string: “<h1 id=”pick-me”>Greeting To <span>All</span>!</h1>”


* .textContent only provides the text of the element
* .innerText returns the text as is seen visually

---

## Create New Elements

* Can use…
	
		document.createElement(‘h1’);

* The h1 will be created but it will not be added to the page.
* To create and add you must use the .appendChild()

		var newSpan = document.createElement(‘span’); // create a span
		var mainHeading = document.querySelector(‘h1’); //select the heading

		mainHeadnig.appendChild(newSpan); //add the newSpan to the heading
	
--- 

## Creating a TextNode

* Creates a paragraph
* Creates a text node
* Appends the text node to the paragraph
* Appends the paragraph to the tag

        Example:

        var myPara = document.createElement(‘p’);
        var textOfParagraph = document.createTextNode(‘I am the text for the paragraph!’);

        myPara.appendChild(textOfParagraph);
        document.body.appendChild(myPara);

        //output: <p>I am the text for the paragraph!</p>

---

## Inserting HTML In Other Locations

Using the .appendChild() method will add an element as the last child of the parent element. 
Can use the insertAdjecentHTML() method to be able to add it in other locations…
Need two arguments…
1. The location of the HTML
    * beforebegin - inserts the HTML text as a previous sibling
    * afterbegin - inserts the HTML text as the first child
    * beforeend - inserts the HTML text as the last child
    * afterend - inserts the HTML text as a following sibling
2. The HTML text that is going to be inserted


        <!-- beforebegin -->
        <p>
            <!-- afterbegin -->
            Existing text/HTML content
            <!--beforeend-->
        </p>
            <!-- afterend-->

            var mainHeading = document.querySelector(‘#main-heading’);
        var htmlTextToAdd = ‘<h2>Skydiving is fun!</h2>’;

        mainHeading.insertAdjacentHTML(‘afterend’, htmlTextToAdd);

---

## Remove Page Content
	
* Removing a child this requires 2 methods...
    1. A parent element
    2. The child element that will be removed

	        <parent-element>.removeChild(<child-to-remove>);

	* You can also remove an element by using the remove() method

            var mainHeading = document.querySelector(‘h1’);
            mainHeading.remove();

--- 

## Style Page Content
	
* We can access an elements style attribute using the .style property
	
        var mainHeading = document.querySelector(‘h1’);
        mainHeading.style.color = ‘red’;
        mainHeading.style.fontSize = ‘2em’; 
        mainHeading.style.backgoundColor = ‘yellow’; 

* Is not font-size is fontSize dashes cannot be used in dot notation because property are identifiers. The - is a keyword for things such as subtraction.

* If writing multiple css styles use the cssText property
	
        var mainHeading = document.querySelector(‘h1’);
        mainHeading.style.cssText = ‘color: red; fontSize: 2em; backgoundColor: yellow’ ;

---

## Using the .setAttribute() 

* This method is not just for styling page elements. Can use this method to set any attribute for an element.

        var mainHeading = document.querySelector(‘h1’);

        //add an id to the heading’s sibling element
        mainHeading.nextElementSibling.setAttribute(‘id’, ‘heading-sibling’);

        //use the newly added ID to access that element
        document.querySelector(‘#heading-sibling’).style.backgroundColor = ‘red’;


* To add or remove a class name use:
    * .classList.add(‘.name’);
    * .classList.remove(‘.name’);
* Other:
    * .toggle() - to add the class if it doesn't exists or remove it from the list if it does already exist
    * .contains() - returns a boolean based on if the class exists in the list or not
