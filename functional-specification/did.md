# DID Sdk Functional Specification

The  decentralized identifiers (DID) library will allow DIDs that can use the NFC device as a verification method. This will allow the DID to authorize and sign verifiable credentials, verifiable presentations and interact with other SSI components.

If the interaction with the NFC device fails (e.g. the NFC device is not presented in time, or the correct PIN is not presented) then an error will be thrown.

## Resolving a DID Document
A DID can be resolved into its corresponding DID Document. This will be achieved through the [Universal Resolver](https://github.com/decentralized-identity/universal-resolver).

The public key on the NFC device will be fetched.  This may require user input of the PIN or other security options. If requested, the public key will be verified by checking that the card presents a signature of a provided random challenge.

The DID document will be inspected and to ensure that a verification method exists with the public key from the NFC device. If the public key cannot be found then an error will be thrown.

If a DID URL is asked to be resolved, then the verification method with the same DID URL will be inspected for the NFC public key.

## Sign
This will sign a string or a json object, using the private key of the NFC device.

If the input is a string, the NFC device will sign a SHA256 hash of this string. If the input is an object, this will be converted into a JSON string and the NFC device will sign a SHA256 hash of this string.

## SignHash
This will sign a hash, using the private key of the NFC device.

## Get Public Key
The public key on the NFC device will be fetched. This may require user input of the PIN or other security options. If requested, the public key will be verified by checking that the card presents a signature of a provided random challenge, which takes a bit more time.

## Not in scope
Configuration of the NFC device is not supported by the library. This should be done directly using the React Native Tangem SDK’s wallet functions.

To ensure the library is fully DID method independant, DID create, update and deactivate operations are not directly supported by the library. This is because each DID method has a different mechanism for these operations. The library provides the `sign()`, `signHash()` and `getPublicKey()` functions to allow for these DID operations to be implemented in their respective DID method implementations if needed. An example application will demostrate how to implement DID create for reference.
