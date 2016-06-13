---
layout: post
title: Javascript Arrays
---

![Javascript Arrays]({{ site.baseurl }}/images/javascript-mutator-methods.png "JavaScript Mutator Methods")

For javascript, <strong>length</strong> was the begin all and end all of manipulating arrays. I'm going to draw out an example first by creating an array and showing what length will give us. The purpose is to how we used length in the "before time" to quote Mad Max and the the new we can accomplish the same goal.

```javascript
var shortArray = ["First", "Second", "Third"];
var total = shortArray.length;
```

We created an array called shortArray that contains "First", "Second", "Third". Along with that we have total as the shortArray length equal 3, the number of times in the array.

This was the way I learned to add an element to the end of an array like shortArray.

```javascript
shortArray[shortArray.length] = "Fourth";
```

Now shortArray contains "First", "Second", "Third", Fourth" and total now equals 4.

Now today the same can be accompliced with "**Mutator Methods**". This one is the **JavaScript push() Method**. **Push** will not just add an item to the end of the array but will also return the array's new **length**:

```javascript
var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.push("Kiwi");
```

This will make the array "Banana", "Orange", "Apple", "Mango", "Kiwi" and returns 4.
