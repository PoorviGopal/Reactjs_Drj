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


## Part 2: Code

```js
import React, { useState } from 'react';

function SGreetingComponent() {
    const [greetingMessage, setGreetingMessage] = useState("Hello, User!");
    
    function changeGreeting() {
        setGreetingMessage("Welcome, User!");
    }
    
    return (
        <div>
            <h1>Experimenting state variable</h1>
            <p>{greetingMessage}</p>
            <button onClick={changeGreeting}>Change Greeting</button>
        </div>
    );
}

export default SGreetingComponent;
```

## Try executing both the code by calling them in App.js

```js
import VGreetingComponent from './components/variable'
import SGreetingComponent from './components/state';
function App(){
return(
      <div>
        <VGreetingComponent />
        <SGreetingComponent />
      </div>
)

}

export default App;
```
