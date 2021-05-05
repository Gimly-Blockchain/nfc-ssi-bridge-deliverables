# Functional overview
The SSI-NFC bridge  consists of two toolsets. These tool sets allow developers to use SSI components that are cryptographically signed or bound to the NFC device, as explained below.

## 1. Software development kit (SDK)
This is a react native SDK  which allows developers to build SSI  applications using the features of the NFC devices. There are three planned libraries to support DIDs, verifiable credentials and verifiable presentations.  These libraries will make  the use of the React Native Tangem SDK and create the abstraction layers on top of this to facilitate easy-to-build SSI applications that take advantage of the secure Tangem NFC devices.

Support for additional SSI components can be added. DIDComm may be supported in the future if sufficient interest is shown.

### Architecture
https://app.diagrams.net/?src=about#Wb!UFIMBWhfz0inZKDnVB8V8m1lWOD-8YNGmmv4QYhxVdO9TgM4_ZGCTKeQbSUIDpY2%2F01ZITDDMEUOERAG5NCJREKAW5OOFALLXSA

As seen in the architecture diagram, the NFC-SSI bridge SDK will use the React Native Tangem SDK to communicate with the Tangem device using the NFC transport protocol. The Tangem device stores a private key, which can be used to digitally sign transactions.

See
DID-functional.md
VC-functional.md
VP-functional.md

### User interface
To facilitate the testing an understanding of the SDK,  we aim to create a simple React Native  application that displays the core functionalities of these libraries.  the user stories of this application can be found here:
User-stories.md 

## 2. Command line interface (CLI)
This is a nodejs package, to be installed locally by developers with a small amount of functions to assist in initialisation and configuration of their React Native project. Their project will then be able to immediately use the Tangem and SSI-NFC bridge SDKs.

This is an optional component, provided for developer convenience so that they do not have to install all the dependencies for using Tangem NFC devices manually, which can be difficult.

See
CLI-functional.md

## Support
The SSI-NFC bridge will support React Native projects, with the same prerequisites as React Native to use.

Additionally, phones will need to have an NFC reader to be able to use these libraries. Desktop clients will need to have an inbuilt or USB NFC reader.




