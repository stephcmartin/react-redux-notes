What is Redux?
Redux is a predictable state container for JavaScript apps.

Plug Any Data Into Any Component
This is the problem that Redux solves.
It gives components direct access to the data they need.
Using the connect function that comes with Redux, you can plug any component into Redux’s data store,
and the component can pull out the data it requires.

Actions
Actions are payloads of information that send data from your application to your store.
They are the only source of information for the store.
You send them to the store using ```store.dispatch()```.

Actions are plain JavaScript objects.
Actions must have a ```type``` property that indicates the type of action being performed.
Types should typically be defined as string constants.
Once your app is large enough, you may want to move them into a separate module.

Action Creators
Action creators are exactly that—functions that create actions.

In Redux, action creators simply return an action:

```function addTodo(text) {
  return {
    type: ADD_TODO,
    text
  }
}
```

To actually initiate a dispatch, pass the result to the ```dispatch()``` function:

```dispatch(addTodo(text))```
```dispatch(completeTodo(index))```

Alternatively, you can create a bound action creator that automatically dispatches:

```const boundAddTodo = text => dispatch(addTodo(text))```

```const boundCompleteTodo = index => dispatch(completeTodo(index))```

Now you'll be able to call them directly:

```boundAddTodo(text)```

```boundCompleteTodo(index)```

The ```dispatch()``` function can be accessed directly from the store as ```store.dispatch()```, but more likely you'll access it using a helper like react-redux's ```connect()```. You can use ```bindActionCreators()``` to automatically bind many action creators to a ```dispatch()``` function.

Action creators can also be asynchronous and have side-effects. You can read about async actions in the advanced tutorial to learn how to handle AJAX responses and compose action creators into async control flow. Don't skip ahead to async actions until you've completed the basics tutorial, as it covers other important concepts that are prerequisite for the advanced tutorial and async actions.

##Reducers
Reducers specify how the application's state changes in response to actions sent to the store. Remember that actions only describe what happened, but don't describe how the application's state changes.
