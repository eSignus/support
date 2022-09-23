---
title: Duplication process
tags: [security]
---

- A user buys one of her duplicate Link Cards from her Issuer. The Issuer knows the user's physical address and phone number.
- The Issuer asks the Customizer for a duplicate Card and sends the contact address and the CardId to them.
  The Customizer uses the CardId access to the database and sends it to the HSM. The HSM decrypts the Recovery Seed, and in an automatic process, both numbers are NFC charged into the Link Card. The next step is to write the destination address on an envelope, put the Card in, and ship it.
