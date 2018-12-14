# Form

This type of content allows you to display interactive Form, that will help you collect informations.


## Content extension

To create a form, put all the items you need in a folder, and add the extension `.form` at the end of the name of your folder.

Inside your folder, provide a file called `_questions.xml`

## <a name="contents"></a>Contents : `_questions.xml`

A form is composed of small elements to present or collect informations : 
* `<input>` to collect informations
* `<presenter>` to display informations

They both can be described with the following attributes :
* `type` : what the element will look like (see sections [Input Types](#input-types) and [Presenter Types](#presenter-types))
* `text` : the title or question displayed above the element
* `tooltip` : adds a question mark button next to the title to display the text given here
* `valuekey` : store and retrieve the value of an input under this key
* `visiblewhen` : show the element only when the condition given is fulfilled (see section [Elements Visibility](#elements-visibility))

## Organize elements
Inputs and presenters can be written in the order of appearance inside the tag `form` or organised into columns thanks to the tag `<section>`

*Examples*
Four inputs displayed in a single column :
```xml
<form>
    <input />
    <input />
    <input />
    <input />
</form>
```

Four elements displayed into two columns :
```xml
<form>
    <section>
        <input />
        <input />
    </section>
    <section>
        <input />
        <input />
    </section>
</form>
```

## <a name="elements-visibility"></a>Elements visibility
You can choose to display an element `X` (input, presenter or section) based on the value of an input `Y` using the attribute `visiblewhen`.
Its value must have the pattern `key``comparator``value(s)`.

The key is the `valueKey` attribute of the input `Y`

The different comparators allow to test :
* equality "="
* difference "!=" 
* numeric comparisons ("<","<=", ">=", ">")
* unstrict containance "=*"

*Examples*
If we have a multiple choice input with the possible answers `A`, `B` and `C`, we can have the following visbility behaviors on an other element :
* `visiblewhen="myKey=A"` : visible if the answer `A` is the only one selected
* `visiblewhen="myKey!=A"` : visible if `B`, `C` or both are selected
* `visiblewhen="myKey=*A"` : visible if at least `A` is selected (`B` and `C` can also be selected)
* `visiblewhen="myKey=B&C"` : visible if `B` and `C` are selected and `A` is not
* `visiblewhen="myKey=B|C"` : visible if `B`, `C` or both are selected and `A` is not


## <a name="input-types"></a>Input Types

### Single choice
### Multiple choice
### Single line text
### Multiple line text
### Slider
### Combobox

## <a name="presenter-types"></a>Presenter Types

### Documents

## Other Values
To allow the user to fill an other value than the ones you present, add a `<choice>` of type `othervalue`.
A `<choice>` of type `novalue` adds a check box under the input to deselect all other answers


