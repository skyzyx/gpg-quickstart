# Installing GPG Tools Suite for macOS

## Download

[GPG Tools Suite][gpgtools]

## Create a New Key

First, open the _GPG Keychain_ and choose _New_.

[![Create a new key](new-key.png)](new-key.png)

Next, fill out the Wizard making certain selections.

* ✓ _Upload the public key_
* Key type should be _RSA and RSA (default)_
* Length should be _4096_.
* Expiration should be any value, but the default value is _4 years from now_.

[![New Key Wizard](new-key-wizard.png)](new-key-wizard.png)

Right-click on your name, and choose _Export…_

[![GPG Listing: Export](gpg-listing-export.png)](gpg-listing-export.png)

Export your key, and save it somewhere where you can share it (e.g., Desktop, Dropbox, iCloud Drive).

* _Include your secret key_ **ONLY IF** you want to backup your secret key. **Never share this with anybody!**

* If you plan to _share your key with someone else, or otherwise make it public_, **UNCHECK the checkbox**.

[![Save Dialog](save-dialog.png)](save-dialog.png)

## Importing a GPG Key

There are different ways to import the key. The **first** is to double-click the `.asc` file.

The **second** is to view the file with QuickLook, then choose to _Open with GPG Keychain…_

[![Quicklook](quicklook.png)](quicklook.png)

The **third** is to open the GPG Keychain, then drag one or more files into its window.

[![Click and drag](click-drag.gif)](click-drag.gif)

## Encrypt a file



  [gpgtools]: https://gpgtools.org
