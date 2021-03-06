##07/16/2014

##Version:
1.2.0

##Added features
- Return 502 Bad Gateway middleware when remote is not connected to rippled.

##Bug Fixes
- 502 Middleware fixes the crash-on-startup bug when clients try to connect before
  ripple rest is connected to rippled.

##07/10/2014

##Version:
1.1.2

##Added features
- Code climate integration badge
- capistrano scripts for server deployment
- new version of ripple-lib

##Bug Fixes
- Setting SendMax on payments
- Fix broken outgoing payments endpoint

##06/18/2014

##Version:
1.1.1

##Added features
- Add Istanbul code coverage tests
- Refactor out express app object
- Add a few integration tests using superagent

##Bug Fixes
- Return 500 instead of 200 on invalid ripple address

##06/11/2014

##Version:
1.1.0

## Added features
- Add exclude_failed option to getAccountTransactions (defaults to false)
- Add protocol, host, and port (when applicable) to URLs returned to client
- Coveralls for testing

###Internal Changes
- Add JsDoc comments to transactions.js, payments.js, and notifications.js
- Centralize ripple-lib transaction submit and get functions in transactions.js
- Significantly simplify getAccountTransactions logic and parameters set by recursive call
- Test ripple-lib transaction functions
- Test transaction submission to ensure transaction is saved to the database every time its state is changed
- Test payment submission and retrieval
- Test notifications
- Move notification and payment formatter functions into notifications.js and payments.js, respectively
- Replace hard-coded server connection timeout value with exported variable in server-lib.js

###Bug Fixes
- Callback with error and entry for function to query database for transaction in getTransactionHelper
- Prevent second HTTP response for error after transaction proposed event in submitTransaction function
- Validate account in getTransaction
- Attach client_resource_id in getTransaction so it is correctly returned to client
- Strange pathfinding error message when no paths are found because of a lack of liquidity

##06/10/2014

###Version:
1.0.2

###Fixed bugs:
- GET /v1/accounts/{:account}/payments/{:hash} not responding

##06/04/2014

###Version: 
1.0.1

###Fixed bugs:
- Client resource id now properly returned
- XRP Pathfind bug
- Pathfinding error message
- missing invoide_id
- normalize account settings 
- notification timestamp formatting

###Added features:
- Travis.yml for Continuous Integration
- License
- Tests for balances, trust lines
- Add debug mode

