Foreach processing and choice routing example with API Kit:
----------------------------------------------

This example is based on the example provided by mule studio (http://www.mulesoft.org/documentation/display/current/Foreach+Processing+and+Choice+Routing+Example).

Changes to the original example:

<ul>
<li>added new mflow: mule-config.mflow: this file contains the global exceptions, the main flow with the apikit router, and two basic flows for get and post Loan Requests
<ul>
<li>post:/request --> receives a json object and transforms to a Pojo (LoanQuoteRequest)</li>
<li>get:/request --> receives the params and creates a Pojo (LoanQuoteRequest)</li>
</ul>
</li>
<li>decomposed the loanrequestflow in several flows
<ul>
<li>http-request-no-apikit: the original flow with the HTTP endpoint</li>
<li>flow-for-get-requests</li>
<li>Main-flow: the original flow but without the request parameters processing and validations </li>
</li>
</ul>

Contact
=======
matias.juan@mulesoft.com
