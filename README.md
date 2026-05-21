**Author** : Prabhmeet Deol

# Overview of How to Setup mTLS in AWS

## Requirement
Typically, if organizations require encrypted service-to-service communication, they would use mTLS over TLS to mutually authenticate both the client and the server (vice versa). 
![mtls Demo By Wallarm](https://lab.wallarm.com/what-is-mtls-the-essential-guide-you-cant-afford-to-miss/)

## Examples
1. A bank trying to authenticate a merchants api, before allowing to process a payment.
2. A hospital`s microservice trying to authenticate a insurance providers microservice.

## References
1. [AWS mTLS authentication on ALB](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/mutual-authentication.html)
