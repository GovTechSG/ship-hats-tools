# Production Risk & Policy Compliance

FOD introduces a system policy which is shown for each FOD application based on the severity of the findings for each release.

Releases are awarded 1-5 stars based on whether any CRITICAL, HIGH, MEDIUM, or LOW findings are found as indicated in the image below:

![Assessment Rating](./images/fod-assessment-rating.png)

Policy compliance is set to FAIL whenever it is lower than 3 stars, which means that there are HIGH and above findings for the release.

![Policy Compliance](./images/fod-policy-compliance.png)
