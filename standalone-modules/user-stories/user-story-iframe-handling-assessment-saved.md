# Client Handling of Assessment Saved

## Purpose:
The client may want to have special logic when using iframes that an assessment has been saved.  One use case is that they wish to add in their own custom logic to trigger an event to update their system for reporting purposes.

The event is a simple post message sent to the window.  This approach vs accepting custom functions was used as the best fit for all clients while mitigating security concerns.

## Example:
The client would need to need to add javascript in the rendered html to pick up the window level event.
````
    <script>
        window.addEventListener('message', (message)=> {
            // Ability Explorer has 
            if(message.data === 'IC_AE_SAVED'){
                // Client's special logic goes here
            }
        });
    </script>
````

## Events:

````IC_AE_SAVED````
This event is emitted when a scored Ability Explorer assessment is saved by the client.