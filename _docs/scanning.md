---
title: Scanning your first HASHWallet Link
tags: [settings]
---

The process is simple for the user but complex internally. We will describe what hAppens from both sides.

## User experience

The user has logged into the eSignus Backup Center Now you will press the SCAN CARD button and place the card as shown on the screen. The position depends on the smartphone. In the following images, we can see the usual place for android phones and iPhones.

![Scanning](https://uc5a89db489904258a29803b7cd1.dl.dropboxusercontent.com/cd/0/inline/BtBpoMhj0OBg0fQI4CZnksdPqiTtGF8IegcDpztQDQ1LFqv887tuNmrrpugBHoliTERNhTM7K4TRAL3C_HvYf0ecp6Gf_h8lDqPESGaV9Q_zxc2xoDYLWA9ty6XqSqzeteHVcUOPECRIEGYZ_AUzBV2BOfDLOb4hcf6EB-ypY3LaNw/file#)

![Scanning](https://ucf4cbec683beb953e2bc21c2ed1.dl.dropboxusercontent.com/cd/0/inline/BtD0KaKWV0WCgH8vGbDHX6Sk7CsYATSaOD1ENl-goEE-mS1D9A2C9A6Hva5Hl81WTfNlGycxSy_wWWlxtZw0-fm-awHvJ46UyXzJ-hRoWFDI9Th7rBngTzBJPDaxswQD3uhjl6XEtfavh0_eHGqY7I8lhL-C2ARCiA9-IJvAadJwuQ/file#)

The next step is to remove the card while the following image appears on the screen. Now we will need to put the card again close to the phone and remove it when the Apps require us to do so.

Voila, the card is included.

## Internal process

We will explain step by step the complete initialization process below.

### First step

You must place the card near the phone; when the NFC antenna detects it, the HW manager star running the following process:

- Ensures the card is correct.
- Asks the card for an encryption public key.
- Asks the card for the Issuer Id.

Now you have to separate the card from the NFC antenna on the phone to finish the first step.

### Second step

To start step two, you must place the card near the phone again, and when the NFC antenna detects it, the HW manager star running the following process:

- Asks the HW Link card to generate the seed randomly and calculate the Recovery Key.
- HW Manager randomly generates a PassPhrase and sends it to HW Link card.
- HW Manager sends to HW Link card the public encryption key.
- HW Manager sends to HW Link card the encrypted UserId and CardName
- HW Manager asks the HW Link card to calculate the HW AES Key using the UserId and the Recovery Seed.
- HW Manager asks to HW Link card to store the FullCardName
- HW Manager asks HW Link card to encrypt the RecoveryInfo file and to send it. It contains Recovery Key, Seed Public Key, and PassPhrase.
- HW Manager asks HW Link card to encrypt the IssuerInfo file and to send it. It contains CardId, CardName and UserId.

Finally, the HW Manager sends the RecoveryInfo file and the IssuerInfo to the Secure Vault in the eSignus Backup Center.

### Third step

To start step three, you must place the card near the phone again, and when the NFC antenna detects it, the HW manager star running the following process:

- HW Manager asks HW Link card to erase Recovery Seed, Recovery Key, UserId, and PassPhrase.
- HW Manager asks HW Link card to store the InitOk state.

The LINK card has been initialized.
