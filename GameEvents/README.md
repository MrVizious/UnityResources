# GameEvents

This system creates custom event named GameEvent that relies on ScriptableObjects for its use.

## How to use it

### Creating a GameEvent

For any new event that could be raised and listened to, create a new Event somewhere in your project hierarcy (/Assets/Events/ is recommended, with specific subfolders if needed) by pressing right click on the project view and then Create -> CustomSO -> Events _> GameEvent.

Now, in the Inspector view, you can activate this GameEvent anytime you want.

### Listening to the GameEvent

Add a new component of type GameEventListener to the GameObject you want to listen to the event. Now, as with any normal UnityEvent, add the expected function to call if the GameEvent is raised.

Make sure the function you want to call is public and the GameObject has been dragged inside the selector of the Response() field.

### Raising the GameEvent

Theoretically, you could just raise the GameEvent from code, but using a UnityEvent is encouraged, so you can easily change the behaviour from the editor.