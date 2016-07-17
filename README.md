# JavaScript Mutation Events

In this example, two events listeners each trigger their own function. The first is on the last but one line, and it listens for when the user clicks the link to add a new item. It then uses DOM manipulation events to add a new element (changing the DOM structure and triggering mutation events). The second event listener waits for the DOM tree within the ul element to change. When the DOMNodeInserted event fires, it calls a function called updateCount function. This function counts how many items there are in the list, and then updates the list count at the top of the page accordingly.

## Problems with mutation events

If your script makes a lot of changes to a page, you end up with a lot of mutation events firing. This can make a page feel slow or unresponsive. They can also trigger other event listeners as they propagate through the DOM, which modify other parts of the DOM, triggering more mutation events. Therefore they are being replaced by mutation observers.

## New mutation observers

Mutation observers are designed to wait until a script has finished its task before reacting, then report the changes as a batch (rather than one at a time). You can also specify the type of changes to the DOM that you want them to react to. But at the time of writing, the browser support was not widespread enough to use them on public websites.

## How to run the app locally?

* In your terminal type:
```
git clone https://github.com/bostonhuman/mutation-events
```
* Open `mutation.html` to run the app.
