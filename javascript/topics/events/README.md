# JavaScript Events

DOM

Bubbling and Capture

`Event` interface

* [Event developer guide](https://developer.mozilla.org/en-US/docs/Web/Guide/Events)
* [Event reference](https://developer.mozilla.org/en-US/docs/Web/Events)
* [`Event` interface @ MDN](https://developer.mozilla.org/en-US/docs/Web/API/Event)
* [Comparison of Event Targets](https://developer.mozilla.org/en-US/docs/Web/API/Event/Comparison_of_Event_Targets)

## Types of Events

currentTarget/this - Element listener was attached to
vs
target - DOM element that was clicked

### Mouse Events

mouseenter

mouseover

mousemove

mousedown

mouseup

click

dblckick

mouseleave

mouseout

## Keyboard Events

keydown

keypress

keyup

Return [`KeyboardEvent`](https://developer.mozilla.org/en-US/docs/Web/API/KeyboardEvent), and use the [value](https://developer.mozilla.org/en-US/docs/Web/API/KeyboardEvent/key/Key_Values) of [`key`](https://developer.mozilla.org/en-US/docs/Web/API/KeyboardEvent/key) (along with booleans `ctrlKey`, and `shiftKey`) to determine which key was involved.

## Considerations

throttle and debounce!

## Binding callbacks

1. As html attribute

        <button type="button" onclick="myFunction()">Button Name</button>

2. assign to DOM, eg element.onclick =

3. addEventListener

4. ...?

