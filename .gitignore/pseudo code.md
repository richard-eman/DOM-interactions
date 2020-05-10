Script is run as soon as head is loaded (first/early on)
Document.addEventListener("DOMContentLoaded", start) is run
Once the HTML is fully loaded, function start is run because of this
Function start runs more event listeners under the function 'bindEventListeners'
A loop is run to quickly add an event listener to every child item of the class element 'board', these children being the div for each dot on the board.
Now whenever the event occurs, the function associated with the event will run
These associated functions will toggle a class for the class element that had the event and run the function updateCounts ()
updateCounts () creates an var/object called totals with the properties of blue, green, and invisible, all of which are set to the number 0.
Each colour in totals goes up depending on how many elements there are with the class name of the corrisponding colour.
displayTotals (totals) function is run at the end of updateCounts () which takes the totals object/var and runs for every number there is in each property of totals (key is the property, the loop gets the value for this property?).
The loop joins the property name (using key) and a string to know the ID of the element that is to recieve the value. The content of this html element is then made equal to the value of a property of the object, totals.