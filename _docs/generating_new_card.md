---
title: Generation process for new Cards
tags: [security]
---

- A user buys a new Link card from an Issuer. The Issuer knows the user's physical address and phone number.
- The Issuer asks the Customizer for a new Card and sends the contact address to them.
- The Customizer uses an isolated HSM to generate a CardId and a Recovery Seed, and in an automatic process, both numbers are NFC charged into the Link Card. The next step is to write the destination address on an envelope, put the Card in, and ship it.
- The CardId and the encrypted Recovery Seed go to a Key Management System without any relationship with the user.
