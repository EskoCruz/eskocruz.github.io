---
published: false
Title: Spread Operator
layout: post
---

Use the built in `arguments` keyword which will contain the `length` of how many arrays you have. Use that as a basis to loop through each array.

    for(var arg = 0; arg < arguments.length; ++ arg)
    {
        var arr = arguments[arg];
    
        for(var i = 0; i < arr.length; ++ i)
        {
             var element = arr[i];
    
             /* ... */
        } 
    }

Now with ES2015 we can use the **The rest operator** to get the arguments list passed to function on invocation and in array destructure. A case when the operator gathers the rest remained after the operation. The **rest operator** is esentually an elipsis.



