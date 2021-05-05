# User Stories

## Dashboard

As a user
I can navigate to all of the screens of the application
so that I can use application

## DIDs

As a user
I can create a DID
So that I can use the application with my NFC device
Note: this will create an a new DID with a public key from the NFC device

## VC and VPs
As a user with a DID
I can create a VC with my first and last name and date of birth signed by my DID
So that I can use my identity with other people

As a user with a VC
I can store the VC on the NFC card privately secured with a PIN
So that I can retrieve it later for use

As a user with a VC
I can read my private VC my from the NFC device by presenting my PIN
So that I can can use my identity with other people

As a user with a VC
I can delete my private VC my from the NFC device by presenting my PIN
So that  nobody can accidentally obtain my identity data from the card I do not plan to use anymore

As a user
I can revoke revoke a VC  by creating a status update document  signed by my DID
So that people verifing the VC can know that it has been revoked

As a user with a VC
I can create a VP signed by my DID
So that I can share my identity with somebody and they can know I sent it

