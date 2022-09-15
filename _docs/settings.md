---
title: An overview of the HWManager settings
tags: [settings]
---
Let’s have a look over the settings. To start here, we have a figure with all the options. The options are divided into parts.

## Manage Cards

### Backup center

Inside the backup center, you can see a glimpse of the email and phone number you have registered. This is important; they are critical to the recovery system. As you can see in the following screenshot, you can see only the first and last characters to avoid any other than you can identify both of them.

Bellow is the registered phone number. You can find the portfolio backups for every added Card. Once you enter one of the cards, you can upload or download the portfolio structure. This is one of the differential characteristics of HASHWallet. If you need to install the HW Manager App on another phone or if you are recovering your Card from a duplicate, we can have the same portfolio structure you uploaded.

### Portfolio backup

eSignus stores an encrypted copy of the generated wallets and their names when you upload the portfolio structure. This structure is simple, only the generation number and last name. And from this structure, nobody can know how many wallets you have and if there are funds or not. All the portfolio backups have the same size and are encrypted.

The encryption and decryption happen inside your Link Card using the internal AES key.

### Scan card

It is another way to add a new Card to your portfolio. It can be a new Card or an initialized Card. After touching over Scan Card, the HW Manager will wait till you put your Card next to the phone and hold it. The process is the same as in [Add your HASHWallet Link to the HW Manager App](/docs/scanning/).

### Order a new card

You can buy a new Card or a duplicate one. The Recovery Seed and CardId will be the same as your previous Card if you select a duplicate Card and different if you choose a new Card.

In both options, an integrated window will open over the manager, redirecting you to the shop. Still, in the second case (duplicate one), you will need to login into your Issuer page and select the Card you want to duplicate. 

## App settings

### Balance currency

Here you can choose the FIAT coin to calculate each cryptocurrency's equivalent value and the total amount, including every coin.

### Biometric authentication

With this setting, the user can activate or deactivate the biometric authentication. If the biometric authentication is deactivated, the user should use passwordless authentication to log in.

### User statistics

User statistics neither store any amount in transaction, funds destination or user id. The statistics sum up (only from users who authorize it) the following ratios and totals (this list is not complete):

- Rejection ratio
- Type of transaction
- Origin and destiny coins in swapping
- Mean value and standard deviation for transactions
- Operations per weekday/week
- etc
