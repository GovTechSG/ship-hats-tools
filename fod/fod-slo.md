# Service Level Objectives

All assessments have a target turnaround time represented by the Service Level Objectives (SLO) of the chosen assessment type. The SLO is specified in business days, based on the Fortify on Demand data center's time zone. The generic Service Level Objectives are:

|Assessment type|SLO time|
|---|---|
|Mobile |1 to 4 business days |
|Dynamic|2 to 3 business days|  
|Static|1 hour to 2 business days|

If an assessment does not meet customary testing requirements, the testing team may pause the SLO timer while waiting for a response from the customer. The testing team is committed to promptly restarting the timer and testing as soon as possible.

If you have additional questions about SLOs and balancing your business timeline with an assessment service level, [contact support](https://docs.developer.tech.gov.sg/docs/ship-hats-getting-started/contact-us).

> **Note:** Service Level Agreements (SLAs) are specific contractual agreements with customers. The turnaround times may differ from defined SLOs. Service Level Agreements are defined in your customer statement of work (SOW) and include targets and liabilities if they are not met.

## Service Level Objective Dates

The SLO start and end dates are defined as follows:

- **Start Date:** The date the application assessment was requested to be started
- **End Date:** The date the results are available

## Service Level Objective Exceptions

A static assessment SLO does not apply to any of the following exceptions:
- Application has not been packaged correctly as per Fortify on Demand best practice guidelines.
- The application payload exceeds 1,000 MB.

A dynamic or mobile assessment SLO does not apply to any of the following exceptions:
- Fortify on Demand is not provided continuous 24-hour per day access and fully operational test credentials to assess the application that is in scope.
- Fortify on Demand is not able to configure security testing tools to use a minimum of fifteen (15) concurrent connections continuously to assess a single application with an average response time of less than 600 ms to an HTTP/HTTPS request.
- Mobile binary is obfuscated or is not prepared as per Fortify on Demand best practice guidelines.
