# node-counterparty-promise

# Summary

Add Promise support to [counterparty](https:/github.com/monaco-ex/node-counterparty/) package.
(Almost all same as to [bitcoin-promise](https:/github.com/rcorbish/node-bitcoin-promise) package.
It is backward compatible with the original package. If no callback function is
passed in to a command a Promise is returned

# Installation

```
npm install counterparty-promise
```

# Example

```
var counterparty = require( 'counterparty-promise' ) ;

var client = new counterparty.Client({
  host: 'localhost',
  port: 4000,
  user: 'rpc',
  pass: 'password',
  timeout: 30000
});

// get running information
client.getRunningInfo()
  .then( function(result){
    console.log( result );
  }) 
  .catch( function(err){
    console.log( err ) ;
  }) ;
```
