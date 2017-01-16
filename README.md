# Usage

## Base
With CssDynamic you can add properties like standard css method of jQuery

**Syntax:**
````javascript
//jQuery standard
$(element).css(property,value)
//jQuery dynamic
$(element).cssDynamic(property,value)
````
You can also pass an object like new standard of jQuery 3

**Syntax:**
````javascript
//jQuery standard
$(element).css({
   property1:value1,
   property1:value1
})
//jQuery dynamic
$(element).cssDynamic({
   property1:value1,
   property1:value1
})
````
The below parameter represents the actions that may perform (default is `add`). The actions can be:
* [add](#add)
* [new](#new)
* [remove](#remove)
* [rename](#rename)
* [renew](#renew)

## Add
You can add a new rule to an existing stylesheet (you can use the follow parameter to select it).
If it doesn't exist it create the stylesheet

**Exemple:**
````javascript
$('.myClass').cssDynamic('color','#DDD','add', 'idStylesheet')

//another use

$('.myClass').cssDynamic({
   'color':'#DDD',
   'font-weight':'bold'
},'add', 'idStylesheet')

//or

$('.myClass').cssDynamic('color','#DDD')
/* `add` like action and `cssDynamic` like id of stylesheet are default parameters */

````
## New
With this action you can create new stylesheet and it will be placed in the end of body

**Exemple:**
````javascript
$('.myClass').cssDynamic('color','#DDD','new', 'newIdStylesheet')
/* `cssDynamic` is default id parameter */
````
##Remove
It's easy to remove "cssDynamic" with this syntax:
````javascript
$().cssDynamic('remove', 'idStylesheetToRemove')
/* `cssDynamic` is default id parameter */
````
##Rename
You can also rename a stylesheet id with another one
````javascript
$().cssDynamic('rename', 'oldIdStylesheet','newIdStylesheet')
````
##Renew
This action deletes an old stylesheet (by id) and it replace the old stylesheet with the newest

**Exemple:**
````javascript
$('.myClass').cssDynamic('color','#DDD','renew', 'idStylesheet')
````
