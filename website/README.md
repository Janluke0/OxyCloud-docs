# Website

The application's frontend is designed as a single-page **React** app. Since all the content is static, the app can be served through an S3 bucket. 

Because of the limitations of the AWS Educate account, some services like CloudFront are not available, so a proper CDN could not be used.
Moreover, the **Cognito User Pool** requires an https connection to perform Sign In redirection and the S3 bucket does not provide it.

In order to achieve the desired result (secure connection) a workaround was put in place.

The idea is to serve the S3 content from an API Gateway endpoint that acts as a Proxy between the final User and the Website.
After the workaround was put in place we were able to expose the S3 bucket securely.