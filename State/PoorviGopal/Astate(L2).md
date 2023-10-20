## Part 1: Code

```js
import React from 'react';

function GreetingComponent() {
    let greetingMessage = "Hello, User!";
    
    function changeGreeting() {
        greetingMessage = "Welcome, User!";
        // here without document.write() it is not possibe to update the message directly in the UI.
        document.write(greetingMessage)
    }
    
    return (
        <div>
            <p>{greetingMessage}</p>
            <button onClick={changeGreeting}>Change Greeting</button>
        </div>
    );
}

export default GreetingComponent;
```
