# Envisioned interoperability
The SSI-NFC Bridge has numerous applications within the eSSIF-lab ecosystem. It is a library that can be _consumed_ by wallet implementations which will allow the wallet to use the Tangem NFC device to sign Verifiable Credentials and other data for SSI components.

Integration of the SSI-NFC bridge brings greater trust, privacy and trust to SSI interactions than with software key management solutions as they are guaranteed that ownly the person who posesses the key can sign the data.

## Presentations Exchange - Sphereon
We are discussing with Spheren to create an integration of the SSI-NFC bridge into the presentation exchange.

## Automated data agreements - iGrant
We are discussing with iGrant to create an integration of the SSI-NFC bridge into the iGrant wallet and exchange.

## Letstrust.org wallet - letstrust
We are discussing with letstrust to create an integration of the SSI-NFC bridge into the letstrust.org wallet.

## Open up - Evernym
We are discussing with letstrust to create an integration of the SSI-NFC bridge into the Mobile SDK and Connect Me wallet.

## Other wallet providers
As explained, our library can be integrated into any compatible library to bring the benefits of a hardware secure key signatures to SSI. We have identified the following wallet providers in eSSIF which will be able to use the SSI-NFC bridge tools.
1. Letstrust.org SSI wallet - SSI Fabric
2. e-Origin wallet - eorigin.eu
3. GAYA SSI wallet - NYM lab
4. SSI4DTM - Joinyourbit
5. SCEP SDK - Domi Labs
6. Dynamic Data Sharing Hub wallet - The Human Colossus Foundation
7. Wordpress plugin - Associazone Blockchain Italia

## eIDAS interoperability

The Tangem NFC device can produce a digital signature that complies to the eIDAS cryptography standards. We plan to ensure our library allows signatures of VCs to be eIDAS compatible and can be issued by Trusted Providers.

This can be achived with the new signature proof type "CAdESRSASignature" complying to the [AdES](https://en.wikipedia.org/wiki/Advanced_electronic_signature) , using a ([CAdeS](https://datatracker.ietf.org/doc/html/rfc5126#appendix-I.2.3)) elliptic curve signature. With this schema, a proof will look like:
```
"proof": {
  "type": "CAdESRSASignature2020",
  "proofPurpose": "assertionMethod",
  "created": "2019-08-23T20:21:34Z",
  "verificationMethod": "did:factom:5d0dd58757119dd437c70d92b44fbf86627ee275f0f2146c3d99e441da342d9f#MIIEEzCCAvugAwIBAgIUJ0hTJswF5BBreQgbEQL8FTLXwHAwDQYJKoZIhvcNAQELBQAwgZgxCzAJBgNVBAYTAk5MMRYwFAYDVQQIDA1Ob29yZC1Ib2xsYW5kMRIwEAYDVQQHDAlBbXN0ZXJkYW0xFDASBgNVBAoMC1Rlc3RDb21wYW55MQswCQYDVQQLDAJJVDEVMBMGA1UEAwwMU2NvdHQgTWFsbGV5MSMwIQYJKoZIhvcNAQkBFhRzbWFsbGV5QHNwaGVyZW9uLmNvbTAeFw0yMDEyMDIxNDMxMDVaFw0zMDExMzAxNDMxMDVaMIGYMQswCQYDVQQGEwJOTDEWMBQGA1UECAwNTm9vcmQtSG9sbGFuZDESMBAGA1UEBwwJQW1zdGVyZGFtMRQwEgYDVQQKDAtUZXN0Q29tcGFueTELMAkGA1UECwwCSVQxFTATBgNVBAMMDFNjb3R0IE1hbGxleTEjMCEGCSqGSIb3DQEJARYUc21hbGxleUBzcGhlcmVvbi5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQDkZfqj459pkdt5GLelamSySQP3owkyYOXW1NLTLr3dC_RzE8x3SRpHQwaRErm0VYvV35JVvubGZgatm5SNsTUHw7Ywrwy-hGFCXo2JOabL0lj3EpkpRPpVS7GXAlMxTvfZihw8IgmA3ZEnhnCYbyfKiCAOmVGLc_dViFTUuk2O6t6gkAdL0MhzU6nCBBariqlwWQxXf7z-nFubBrBio2l_GL6Pf6orvB_67V2PQEYnYlf24VtfdV34_QcU3T9bQjN2RhSzT9HYrYZtEXEmS4ARaN4mSoCnkITNsrGUz3LpX0ozxk2kQCUe89v8TUd-uYzA_sHXJXa7oHqTA1ZJVrtDAgMBAAGjUzBRMB0GA1UdDgQWBBT2b43zVAuqVWwFIZLSTSOdI3n5IDAfBgNVHSMEGDAWgBT2b43zVAuqVWwFIZLSTSOdI3n5IDAPBgNVHRMBAf8EBTADAQH_MA0GCSqGSIb3DQEBCwUAA4IBAQBnKynE3w04FyEHpYJs94eYrvKAgH6lvavHlDbiZxq1YgPwQN7lbFKIyZxsfcx1QGu1Rk_e-B7D-peIYGtL0-lQxbC88ogh03CaPqrJEhhmSxLEN-L3HQl-pItVUTKH8kaxHeC86ym2pOEJW2y7mVtPYkrgMiTjmOJj60hJEQE87VT_TB_soAXOm8oVXy1Ha3HwHZ4vouG_SwYhXWaqnOUDOifR579Cy53sMkuG0m7SuXxOZp20jnX7TaR8ElH8mZifTSBjkT2RNj1QhFG-Tl5nR_Q63j4xIw9f2Sj-jVclsuIcEQh00bo8pfdMhA-sMX1zCsOvG3sDnsfsqLmL7guV",
  "cades": "-----BEGIN PKCS7----- iG9w0BCRABCaB0MHICAQAwDQYLK... -----END PKCS7-----"
}
```

We are in discussion with the SSI-eIDAS Bridge ([SEB](https://gitlab.grnet.gr/essif-lab/infrastructure/validated-id/seb_project_summary)) team to ensure this interoperability.