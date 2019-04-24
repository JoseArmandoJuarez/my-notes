# The Document Object Model - Otherwise known as the DOM.

## Select Page Element by ID

	document.getElementById(‘logo-brand’);

## DO NOT …
	document.getElementById(‘#logo-brand’);

---

## Select Page Element By Class or Tag

	document.getElementByClassName(‘logo-brand’);
		
	document.getElementByTagName(‘logo-brand’);

*  To be able to select all the elements with either the ClassName or TagName, make sure to add an ‘s’ to the getElement… 

        document.getElementsByClassName(‘logo-brand’);
        document.getElementsByTagName(‘p’);

---

## More ways to access elements

* Can use the querySelector  if only selecting one element it can be a class or an id or a tag name but it only returns the first element that it finds
Make sure to include the ‘#’ for the id or the ‘.’ for the class just like we do with CSS

        document.querySelector(‘#log’); //find and return id element
        document.querySelector(‘.image-size’); //find and return the first class element

        //this is a tag, no need to write <p>
        document.querySelector(‘p’); //find and return the first paragraph element

* To select multiple use the querySelectorAll this will return all elements with the exact name.
Make sure to include the ‘.’ for a class just like we do with CSS

        querySelectorAll(‘.class-name’); //find and return classes with the name ‘class-name’
        querySelectorAll(‘p’); //find and return all the paragraph tags

        
* Example: Write the .querySelectorAll() code to find all paragraph elements that are descendents of elements that have the class articles

        document.querySelectorAll(“.articles p”);
