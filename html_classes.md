HTML Classes
============








##### Add/remove classes using JavaScript or jQuery

###### JavaScript

- `classList` property of elements
    - `contains()`
    - `add()`
    - `remove()`

e.g. 

    var myClasses = document.getElementByID("id1").classList;
    if (myClasses.contains("class1")) {
        myClasses.remove("class1");
    } else {
        myClasses.add("class2");
    }

###### jQuery

- `hasClass()`
- `addClass()`
- `removeClass()`
- `toggleClass()`

e.g.

    $("#id1").hasClass("class1");
    $("#id1").removeClass("class1");
    $("#id1").addClass("class2");
    $("#id1").toggleClass("class1");
    

##### Add/remove classes using jQuery

