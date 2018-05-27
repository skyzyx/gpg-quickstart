# Quickstart information for installing GPG

## What is GPG?

In practice, **Person A** uses GPG to encrypt messages or data so that only **Person B** can read/use them. This is done by using a public key which essentially says that "I am who I say I am."

You need a copy of the public key for the person you want to secure the message/data for. This is conceptually similar to needing a person's phone number before you can call them, or a person's email address before you can send them email.

From [Wikipedia](https://en.wikipedia.org/wiki/GNU_Privacy_Guard):

> GnuPG is a hybrid-encryption software program because it uses a combination of conventional symmetric-key cryptography for speed, and public-key cryptography for ease of secure key exchange, typically by using the recipient's public key to encrypt a session key which is only used once. This mode of operation is part of the OpenPGP standard and has been part of PGP from its first version. […]
>
> GnuPG encrypts messages using asymmetric key pairs individually generated by GnuPG users. The resulting public keys may be exchanged with other users in a variety of ways, such as Internet key servers. They must always be exchanged carefully to prevent identity spoofing by corrupting public key ↔ "owner" identity correspondences. It is also possible to add a cryptographic digital signature to a message, so the message integrity and sender can be verified, if a particular correspondence relied upon has not been corrupted.

## Download GPG for your platform
 
|   | Recommended Software | Notes; Alternate software |
| - | -------------------- | ------------------------- |
| macOS | [GPG Tools Suite][gpgtools] | Alternatively, you can install the _command-line_ version of GPG using [MacPorts] or [Homebrew]. Look for the `gpg2` package. |	
| Windows | [gpg4win], Git Bash | Git Bash includes gnugpg and is available in the command line. |
| Linux | `gpg2` comes pre-installed on modern Linux distributions| Instructions for [RHEL, CentOS, Amazon Linux, Oracle Linux][install-rhel], [Ubuntu][install-ubuntu], [Debian][install-debian], [Upstream GnuPG project downloads][install-upstream] |
| Keybase | See child page…	| |

## Generate a GPG Key Via Command Line

```bash
# make a key (if you don't already have one)
gpg --gen-key
 
... RSA and RSA is okay ...
... 2048 bits is okay ...
... 1y is okay (but choose your own duration) ...
... Real name: First Last ...
... Email address: me@email.com ...
 
# lookie in here
cd ~/.gnugpg
 
# generate an ASCII output of your public key
gpg --armor --output first_last.asc --export 'First Last'
```

  [gpg4win]: https://www.gpg4win.org
  [gpgtools]: https://gpgtools.org
  [Homebrew]: https://brew.sh
  [install-rhel]: https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/7/html/Security_Guide/sec-Encryption.html#sec-Creating_GPG_Keys
  [install-ubuntu]: https://help.ubuntu.com/community/GnuPrivacyGuardHowto
  [install-debian]: https://keyring.debian.org/creating-key.html
  [install-upstream]: https://gnupg.org/download/index.html
  [MacPorts]: https://www.macports.org
