# Understanding Questions:
1. What are the steps of execution from the pressing of the 1 button to the rendering of our updated value? List what part of the code excutes for each step.
* The user presses the 1 button.
* onClick attribute fires anonymous function.
* Anonymous function inside onClick fires dispatch function.
* Dispatch function fires addOne function.
* addOne function returns object containing key `type` with variable value `ADD_ONE`, which has value of string "ADD_ONE".
* Reducer function is called with arguments of state as `state` and object returned by addOne function as `action`.
* Switch block inside reducer function executes on the value of `type` inside action object, which is `ADD_ONE`.
* Switch block inside reducer function evaluates case `ADD_ONE` and returns an object containing a spread of `state`, also assigning `total` to `state.total + 1`.
* Return statement exits switch block and reducer function, setting state to returned object containing new state.
* React renderer detects that state within useRender has been re-assigned to a different reference, and re-renders the UI.
* TotalDisplay shows the total plus 1.
