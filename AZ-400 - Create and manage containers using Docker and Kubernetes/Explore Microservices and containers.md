# Microservices and containers

Microservices is an approach to application development. Every part of the application is deployed as a fully self-contained component, called a microservice, that can be individually scaled and updated.

# Example scenario for Microservices

Imagine that you're part of a software house that produces an extensive monolithic financial management application to migrate to a series of microservices.

The existing application would include the code to update the general ledger for each transaction, and it would have this code in many places throughout the application.

If the schema of the general ledger transactions table is modified, it would require changes throughout the application.

By comparison, the application could be modified to make a notification that a transaction has occurred.

Any microservice that is interested in the transactions could subscribe. In particular, a separate general ledger microservice could subscribe to the transaction notifications and then do the available ledger-related functionality.

If the table schema that holds the general ledger transactions is modified, only the general ledger microservice should be updated.

If a particular client organization wants to run the application and not use the general ledger, that service could be disabled. No other changes to the code would be required.