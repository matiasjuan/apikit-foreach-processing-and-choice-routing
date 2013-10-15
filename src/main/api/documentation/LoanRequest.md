
The main loanbroker flow that:

* Receives a customer request
* Performs a lookup of the customer credit profile using a component binding
* Determines the bank that should be used to request quotes
* Sends the request to the selected banks and aggregates responses
* Selects the lowest quote from the list of quotes
* Returns the response to the client

