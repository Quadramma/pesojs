# Peso (3.99kb)

Minimalistic Lib for Jquery remplacement.

## Features

 - DOM Selector
 - CSS setter
 - Attributes setter
 - Events on / off
 - Brew library integrated (dom builder)

### Examples
```javascript
//Create a Selector.
    var $allDivsElements = $('div');
    var $myBody = $('body');
//Iterate over the selection
    var $allDivsElements = $('div');
    $allDivsElements.each(function(domElement,context){
        domElement.innerHTML = '';
    });
//Accessing DOM element through the selector
    var myDomElementDiv = $('#myDiv').value[0];
//or
    $('#myDiv').first();
//Setting attributes.
    $('#bg').att({
        src:'background.jpg'
        class:'myFirstBackground'
    });
//Setting a canvas width and height.
    var myCanvasSelector = $('#myCanvas');
    myCanvasSelector.css([
        'width:'+window.innerWidth+'px',
        'height:480px'
    ]);
//Create an image selector and append to body using chainability.
    var $ImageSelector = $.create('img#myImage').appendTo($('body'));

//Reusing a Selector
    var $selector = $();
    $selector.select('body').css(['background:red;']);
    $selector.select('div').att({class:'commonDiv'});
    
//Register / Unregister event
var fnResize = function(){}
$('body').on('resize',fnResize);
$('body').off('resize',fnResize);

//Extend the Selector features (plugins)
$.fn.getLength = function(){
    return this.value.length;
}
var numberOfDivs = $('div').getLength();
```

As you can see, the lib ss missing a lot of features but cover some basic things.
Any suggestion is well appreciate!.

###Important note:

[DOMBrew](https://github.com/glebm/DOMBrew) is integrated for DOM Building.


License
----

MIT


