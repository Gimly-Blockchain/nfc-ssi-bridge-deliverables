# Interface
The interface for the SDK and CLI toolsets are the provided in two formats

## Typescript
The [typescript](https://www.typescriptlang.org) type files show tightly coupled semantic interfaces for all variables and functions.  Interfaces are also annotated using [JSDoc](https://jsdoc.app). Interfaces for the sdks can be viewed here:
<br>
[https://gitlab.grnet.gr/essif-lab/infrastructure_2/gimly/SSI_NFC_Bridge/-/blob/master/services/ssi-nfc/types.d.ts](https://gitlab.grnet.gr/essif-lab/infrastructure_2/gimly/SSI_NFC_Bridge/-/blob/master/services/ssi-nfc/types.d.ts)


This can be best viewed in most modern IDE such as Atom or Visual Studio which linked types to other packages such as vc-js and tangem-sdk-react-native can be inspected. Or it can be viewed in Gitlab.

## Markdown
A copy of the interface descriptions made using [JSDoc](https://jsdoc.app) can be found here in gitlab for convenience. This can be viewed in the following files:

[JSDoc](https://jsdoc.app) has the following format and syntax:
```js
/**
* Description of function
*
* @param {ParameterType} [parameterName = optionalDefaultValue] - Description of parameter. [] is an optional parameter.
* @return {ReturnType} - The return value and type, and a description of what is returned
```

- [did.md](./did.md)
- [vc.md](./vc.md)
- [vp.md](vp.md)
- [cli.md](cli.md) // Did we exclude this?
