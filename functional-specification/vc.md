# Verifiable Credentials Sdk Functional Specification

The Verifiable Credentials (VC) library will allow VCs to be issued and revoked using digital signatures from the NFC device, and for VCs to be stored as files on the NFC device. These files can be public meaning anybody with an NFC reader can see the contents, or private meaning that a PIN must be presented to see the contents.

If the interaction with the NFC device fails (e.g. the NFC device is not presented in time, or the correct PIN is not presented) then an error will be thrown.

## Issuing a VC
This will create a VC with a proof containing a digital signature from the NFC device.

## Revoking a VC
This will create a [VC status update document](https://w3c-ccg.github.io/vc-csl2017) with a proof containing a digital signature from the NFC device.

This is still an experimental part of the VC specification, and may need more maturity before it can be implemented.

## Store a VC file
This will store a VC as a file on the NFC device. This file can be public meaning anybody with an NFC reader can see the contents, or private meaning that a PIN must be presented to see the contents.

## Read a VC file
This will read a specific VC for a given ID from the NFC device. If the file is private then a correct PIN must be presented.
/* I believe the way the demo works now is that only visible/public VC files are shown when tapping
* the card and private files are not shown – and there is no PIN asked. This is how a holder can
* manage which credentials to show or not. But in this case, perhaps you are thinking about a use case
* where a verifier requests a specific VC which may be protected by pin?
* /

## Remove a VC file
This will remove a specific VC for a given ID from the NFC device. If the file is private then a correct PIN must be presented.

## Not in scope
VC operations That do not involve the NFC device are not included in this library. Developers should use the [React Native vc-js](https://github.com/Sphereon-Opensource/react-native-vc-js) or other VC  library for this.
