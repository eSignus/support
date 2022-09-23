---
title: Glossary
tags: [help]
---

## AES encrypted file

All data stored in eSignus Backup Center is encrypted with a 128 AES Key. This AES key is deterministically generated from the Recovery Seed.

AES (Advanced Encryption Standard) is a symmetric encryption standard approved by the NIST (National Institute of Standards and Technology). Attacks have been published that are computationally faster than a full brute-force attack, though none are computationally feasible

## Deterministic calculation

Any type of calculation which obtains the same result when using the same data.

## Master seed

It is the root seed of the deterministic wallet structure. From this seed and the passphrase every wallet can be derived. This value and the Card Id are the only values that need to be stored securely inside the Secure Element of an initialized HW Link Card.

## Recovery Key

The recovery Key is calculated from two random values, the master seed and the recovery seed. This calculations only happens once, in the initialization process. During this initialization process the HW Link Card encrypts the recovery key and stores it in the eSignus Backup Center.

When a users needs to duplicate a HW Link Card she will need a pre-initialized card (containing the recovery seed and the card Id) and the recovery key (obtained from the eSignus account).

## Recovery Seed

This is a random 256 bits number generated in the customizer HSM. This value and the Card id are the only values included in a pre-initialized HW Link Card.
When you buy a new card this values are random, but when you buy a duplicate one this values are recovered from the Key Management System. Remember this values have no relation with your wallets if the Recovery Key is not present.

## PassPhrase

What happens if you lose your HW Link Card and someone finds it (or they stole it from you)? That card is useless without the passphrase.
Where is the passphrase? It is stored in the Manager App, never in the HW Link Card.
Do I need to remember the passphrase? No, you do not even need to know the passphrase exists.
What happens if I spawn a new instance of the Manager App? The passphrase downloads from the eSignus Backup Center transparently (AES encrypted). It is decrypted within the secure element and passed to the Manager application.

## Public encryption key

Every communication with the HW Link Card is encrypted. Before this communication starts a handshake protocol starts and public keys are sent. Both sides in the communication encrypt with their private keys and the receiver decrypts it with the public key.
