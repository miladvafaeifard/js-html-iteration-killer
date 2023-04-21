# Don't use HTML Iteration that will destory your computer

a NodeList that looks like an array, actually it’s not. It’s a
live collection that is being updated with every DOM reflow. If we add a new element to the live collrection will cause an infinite loop.

So it is important to know that on iteration through a live collection (NodeList, HTMLCollection) is slow and considerably resource-expensive.

a solution is to that is just to convert the collection into an array such as the following example:

```js
  [].slice.call(nodeList)
```
or can be done with the spread operator:

```js
  [...nodeList] 
```


References:
- https://gomakethings.com/live-vs.-static-nodelists-and-htmlcollections-in-vanilla-js/
- JavaScript Unlocked (2015)

[Edit on StackBlitz ⚡️](https://stackblitz.com/edit/js-jvl6gu)