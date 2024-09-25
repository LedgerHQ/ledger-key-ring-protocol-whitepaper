# Ledger Key Ring Protocol White Paper

Welcome to the GitHub repository for the Ledger Key Ring Protocol White Paper! This repository contains the complete text of the technical white paper that delves into the system design, architecture, and operational flows of Ledger Key Ring Protocol (LKRP).

## Overview

The purpose of this repository is to provide open access to the detailed examination of LKRP, with a strong focus on its design and security goals.

The Ledger Key Ring Protocol enables multiple applications or multiple instances of the same application to access a shared secret used to encrypt and decrypt data. Typically, when multiple applications share a secret, sharing the secret with an additional application means re-encrypting the entire data set.  In many instances, this is impractical, if not completely infeasible. 
Instead, Ledger Key Ring Protocol allows decentralized data management without committing to a single storage method.

**Key Features and Design Goals:**
- **Selective Disclosure**: Ledger Key Ring Protocol lets you share selected data with other entities. This is crucial in decentralized applications where trust in centralized servers is not possible. Instead of encrypting the data as a whole, we split it into shards, then encrypt each field with its own encryption key (e.g. each field of a JSON document would have its own encryption key). This data is then safe to share across decentralized networks. Other applications can retrieve and decrypt the data only if they obtain the appropriate encryption keys from the user. The user is in control and decides who can decrypt his/her data.
- **Decentralized Key Management**: Unlike traditional centralized systems, where a central server manages keys and data, Ledger Key Ring Protocol relies on a decentralized approach. Using a key derivation tree based on the BIP32 key derivation standard in Bitcoin, Ledger Key Ring Protocol can generate an infinite number of secrets from a single source. This ensures that new participants can be added without having to re-encrypt the entire dataset.
- **Enhanced Security with Secure Devices**: Ledger Key Ring Protocol leverages secure devices to manage access to secrets. These devices, although limited in memory and computational power, provide robust security by ensuring that sensitive operations occur within the device without exposing the secrets. It allows the user to keep control over their data and choose who has access to what.
- **Efficient Key Revocation and Identification**: The protocol includes mechanisms to handle key revocation, a critical feature when a third party is no longer trusted. Ledger Key Ring Protocol’s structured derivation path allows for efficient key management and identification of resources behind an encryption key, meaning you can review which data you’re sharing and easily revoke an application’s access when necessary.


## Contents

In this repository, you will find a PDF version of the [white paper](Ledger%20Key%20Ring%20Protocol%20Technical%20White%20Paper.pdf).

## Contributing

While the white paper is primarily an informational document, we welcome any corrections or suggestions for improvement. If you spot a typo, a sentence that could be clearer, or even a significant error in our explanations, please raise an issue.
