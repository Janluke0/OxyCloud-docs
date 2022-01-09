# Authorization
Authentication and authorization are performed using the **AWS Cognito User Pool** service.
The user pool contains general user information such as *username*, *email* and *password* as well as two custom attributes defined to restrict user access to specific resources and services (*company*, *subscription_plan*).

Both the attributes are set by two **AWS Lambda functions** which are triggered by User Pool events.

As the User attempts to Sign Up to OxyCloud, the *verifySubscriptionPlan* Pre-Signup lambda function gets triggered. The function verifies the provided subscription plan and writes a DynamoDB record in the User Plan Table specifying the chosen subscription plan.

For semplicity sake, the user email gets auto-confirmed by the system that immediately invokes the *setUserCompany* Post-confirmation Lambda function.
The function extracts the company name from the domain provided in the user email and updates the *company* field in the User's User Pool record.

The use of these two Lambda functions let us remove *write* permissions for business-logic important attributes such as *company* and *subscription_plan* from the client.