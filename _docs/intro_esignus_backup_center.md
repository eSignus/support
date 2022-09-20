---
title: eSignus Backup Center
tags: [settings]
---

## What is eSignus Backup Center?

It is a cloud vault service that securely stores some elements that allows a secure backup and recovery solution.

When using HASHWallet cards, you only need to worry about the transactions you need, but neither about security or recovery issues nor your wallets' setup. Everything is stored securely in a distributed organization.

The eSignus Backup Center stores the following information:

- Recovery Backup (AES encrypted file)
  - Recovery Key
  - PassPhrase
- Wallets Setup (AES encrypted file)
  - For each wallet: Name, Coin, number of the wallet.
- For each card
  - CardName (random id generated during initialization)
  - Alias Name, the cool name you assigned to the card

You will use (in a transparent way) the eSignus Backup Center every time you:

- Initialize a new card
- Recover a duplicate of an already initialized card
- Upload or download a backup of the portfolio and assets setup.
- Request for a duplicate.

Security in accessing the eSignus Backup Center is a cornerstone of HASHWallet, so we need nobody, but you can access it without problem in any (the worst) circumstance. HASHWallet uses a passwordless system based on an email or a phone number. We will ask you to verify both.

For security reasons, once a card is added to the eSignus Backup Center, it will be necessary to validate the edition of the access data (email and telephone number) using any of the added cards to authorize the change of this data.

## Email address verification code

The HW Manager App will ask you for an email address. After that, you will receive a verification code in the email to confirm it is yours.

## Phone number verification code

The HW Manager App will ask for your phone number. After that, you will receive an SMS to confirm it is yours.

## Biometric App unlock

You can activate the biometric used in your phone to unlock the App and avoid entering the verification process for every login. If you uninstall the App or use another phone, you must complete the verification process.
