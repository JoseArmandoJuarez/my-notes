## adding a event listener

* .addEventListener() method let us listen for events and response to them.
    * Listen for an event
    * Listen to an event
    * Hook into an event
    * Respond to an event

* Syntax

        <event-to-listen-for>.addEventListener(‘event-to-listen-for’, function(){
            //function to run when an event happens
        });

        Example:

        document.addEventListener(‘click’, function(){
            console.log(‘the page was clicked’);
        });

---

## Removing an event Listener
* The .removeEventListener() method removes an event handler that has been attached with the addEventListener() method.

* Syntax:

        <event-target>.removeEventListener(‘event-to-listen-for’, function(){
            //do something
        });

        Example:

        function name(){
            console.log(‘Hi’);
        }

        //adds a listener for clicks to run the event function
        document.addEventListener(‘click’, name);

        //immediately removes the click listener that should run the event listener
        document.removeEventListener(‘click’, name);

