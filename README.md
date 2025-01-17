# React Softphone

>

[![NPM](https://img.shields.io/npm/v/tmp.svg)](https://www.npmjs.com/package/tmp) [![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)

## Install

```bash
npm install --save react-softphone
```

## Usage

```jsx
import React from 'react'
import { SoftPhone } from 'react-softphone'
import { WebSocketInterface } from 'jssip';

  const config = {
    domain: 'sip-server@your-domain.io', // sip-server@your-domain.io
    uri: 'sip:sip-user@your-domain.io', // sip:sip-user@your-domain.io
    password: 'secret', //  PASSWORD ,
    ws_servers: 'wss://sip-user@your-domain.io:8089/ws', //ws server
    sockets: new WebSocketInterface('wss://sip-server@your-domain.io:8089/ws'),
    display_name: '***',//jssip Display Name
    debug: false // Turn debug messages on

  };
const setConnectOnStartToLocalStorage =(newValue)=>{


//Save newValue of connect on start to local storage

return true
}

function App() {
  return (
    <div className="App">
      <header className="App-header">
         <SoftPhone
                     callVolume={33} //Set Default callVolume
                     ringVolume={44} //Set Default ringVolume
                     connectOnStart={false} //Auto connect to sip
                     config={config} //Voip config
                     setConnectOnStartToLocalStorage={setConnectOnStartToLocalStorage} // Callback function
                   />
      </header>
    </div>
  );
}

export default App;

```

## License

MIT © [dionis](https://github.com/dionis)

---

This hook is created using [create-react-hook](https://github.com/hermanya/create-react-hook).
