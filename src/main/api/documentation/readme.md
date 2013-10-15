Foreach processing and choice routing example with API Kit:
----------------------------------------------

This example is based on the example provided by mule studio (http://www.mulesoft.org/documentation/display/current/Foreach+Processing+and+Choice+Routing+Example).

Changes to the original example:

* added new mflow: mule-config.mflow: this file contains the global exceptions, the main flow with the apikit router, and two basic flows for get and post Loan Requests
** post:/request --> receives a json object and transforms to a Pojo (LoanQuoteRequest)
** get:/request --> receives the params and creates a Pojo (LoanQuoteRequest)
* decomposed the loanrequestflow in several flows
** http-request-no-apikit: the original flow with the HTTP endpoint
** flow-for-get-requests
** Main-flow: the original flow but without the request parameters processing and validations 
