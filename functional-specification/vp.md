# Verifiable Presentations Sdk Functional Specification

The Verifiable Presentations (VP) library will allow VPs to be created using digital signatures from the NFC device.

If the interaction with the NFC device fails (e.g. the NFC device is not presented in time, or the correct PIN is not presented) then an error will be thrown.

## Creating a VP
This will create a VP with a proof containing a digital signature from the NFC device.

## Not in scope
VP operations That do not involve the NFC device are not included in this library. Developers should use the [React Native vc-js](https://github.com/Sphereon-Opensource/react-native-vc-js) or other VP  library for this.