# DID Sdk Interface

```json
/** 
* Resolves a DID to a DID Document and verifies the DID Document contains a key which can be signed by the presented NFC device
* 
* @param {string} did - A DID or a DID URL string. If this is a DID URL then only the verification method corresponding to the URL will be checked for the key.
* @param {boolean} [verifyKey = false] - If true, the NFC device will be asked to prove it has the private key corresponding to it's private key which is a bit slower.
* @param {OptionsCommon} [options] - Parameters required to interact with the NFC device such as the PIN
* @return {DIDDocument} - The resolved DID Document
*/
resolve(did: string, verifyKey: boolean = false, options?: OptionsCommon): Promise<DIDDocument>

/** 
* Signs data for VCs, VPs, DIDComm 2.0, and blockchain transactions with the NFC device
* 
* @param {string | object} data - A string or object to be hashed and then digitally signed
* @param {OptionsCommon} [options] - Parameters required to interact with the NFC device such as the PIN
* @return {DIDDocument} - A digital signature of the hashed data
*/
sign(data: string | object, options: OptionsCommon): Promise<string>

/** 
* Reads the public key of the NFC device and optionally cryptographically verifies the public key actually exists in the card
* 
* @param {boolean} [verifyKey = false] - If true, the NFC device will be asked to prove it has the private key corresponding to it's private key which is a bit slower.
* @param {OptionsCommon} [options] - Parameters required to interact with the NFC device such as the PIN
* @return {Card} - The details about the card including card ID, public key and more
*/
getPublicKey(verifyKey?: boolean = false, options?: OptionsCommon): Promise<Card>
```