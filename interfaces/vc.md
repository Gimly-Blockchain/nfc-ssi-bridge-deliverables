# Verifiable Credentials Sdk Interface


```js
/** 
* Issues a VC signed by the NFC device
* 
* @param {VerifiableCredentialUnsigned} vc - An unsigned VC
* @param {OptionsCommon} [options] - Parameters required to interact with the NFC device such as the PIN
* @return {VerifiableCredential} - The signed VC
*/
issue(vc: VerifiableCredentialUnsigned, options?: OptionsCommon): Promise<VerifiableCredential>

/** 
* Generated a status updated document signed by the NFC device which can be used to revoke a VC
* 
* @param {StatusUpdateUnsigned} statusUpdate - An unsigned status update
* @param {OptionsCommon} [options] - Parameters required to interact with the NFC device such as the PIN
* @return {StatusUpdate} - The signed status update
*/
async revoke(statusUpdate: StatusUpdateUnsigned, options?: OptionsCommon): Promise<StatusUpdate>

/** 
* Saves a VC as a file on the NFC device, which can be public or private (protected by PIN2)
* 
* @param {VerifiableCredential} vc - A VC object
* @param {OptionsCommon} [options] - Parameters required to interact with the NFC device such as the PIN
*/
store(vc: VerifiableCredential, options?: OptionsCommon): Promise<void>

/** 
* Reads a VC file from the NFC device. If it is a private file a correct PIN2 must be presented
* 
* @param {string} id - The ID of the VC to be read
* @param {OptionsCommon} [options] - Parameters required to interact with the NFC device such as the PIN
* @return {VerifiableCredential} - The VC object
*/
read(id: string, options?: OptionsCommon): Promise<VerifiableCredential>

/** 
* Removes (deletes) a VC file from the NFC device. If it is a private file a correct PIN2 must be presented
* 
* @param {string} id - The ID of the VC to be removed
* @param {OptionsCommon} [options] - Parameters required to interact with the NFC device such as the PIN
*/
remove(id: string, options?: OptionsCommon): Promise<void>
```