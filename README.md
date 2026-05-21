**Author** : Prabhmeet Deol

# Overview of How to Setup mTLS in AWS

## Requirement
Typically, if organizations require encrypted service-to-service communication, they would use mTLS over TLS to mutually authenticate both the client and the server (vice versa). 
![mtls example](./assets/images/mTLS-connection-workflow.jpg)

## Examples
1. A bank trying to authenticate a merchants api, before allowing to process a payment.
2. A hospital`s microservice trying to authenticate a insurance providers microservice.

## AWS Architecture
![mtls example](./assets/images/aws-architecture.png)

In the above example we can configure the mTLS certificate at the ALB, and then only allow authenticate traffic for a distributed system. Additionally, ALB allows to pass X.509 embedded certificate information as **X-Amzn-Mtls-\*** http header to the downstream microservices for consumption.

## References
1. [AWS mTLS authentication on ALB](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/mutual-authentication.html)

2. mTLS connection workflow image source: [AWS Blog - mTLS connection workflow](https://d2908q01vomqb2.cloudfront.net/fe2ef495a1152561572949784c16bf23abb28057/2024/02/01/mTLS-connection-workflow.jpg)
