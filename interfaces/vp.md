# Verifiable Presentations Sdk Interface

```json
/** 
* Issues a VP signed by the NFC device
* 
* @param {VerifiablePresentationUnsigned} vc - An unsigned VP
* @param {OptionsCommon} [options] - Parameters required to interact with the NFC device such as the PIN
* @return {VerifiablePresentation} - The signed VP
*/
create(vp: VerifiablePresentationUnsigned): Promise<VerifiablePresentation>
```