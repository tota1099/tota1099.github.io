---
title: Hash vs Encryption - What's the difference?
slug: hash-vs-encryption
images:
  - /media/criptografia.jpg
date: 2021-02-02T22:05:29.892Z
description: "Hashing and encryption are not the same thing. A simple explanation of what each one is, what it's for and how they differ."
categories:
  - Technology
tags:
  - cryptography
  - security
---
This weekend, June 10, 2018 (yes, this article was written almost 2 years ago), I attended a programming event called PHPSC (https://www.phpsc.com.br/). It was a time of a lot of learning and fun, and I met great people.

Among the talks, one caught my attention: Vinicius Campitelli's (@vcampitelli) talk about Libsodium, a cryptography library that has been part of the PHP core since PHP 7.2. The library has several advantages: it's modern and easy to use for encrypting and decrypting, building password hashes, among other things. I won't go into details about it, but if you're curious you can take a look by clicking [here](https://paragonie.com/book/pecl-libsodium/read/00-intro.md).

In tech it's very common to hear people talking about concepts like encryption and hashing, but many people - even professionals in the field - don't know exactly what the difference is. On top of that, people outside the field end up hearing these terms with no idea what they mean. The goal of this short article is to explain each one in a simple way.

### Encryption

Encryption is the practice of using rules to encode and decode information, so that only people who know the rules are able to encode or decode it.

#### Example

Renan wants to send a secret message to Eduarda. So they agree that the message will be encoded by shifting each letter 2 positions forward in the alphabet (A becomes C, M becomes O, etc.).

Message: MerryXmas

Encoded message: OgttaZocu

Since only Renan and Eduarda know the rules, only the two of them can encode and decode the information and read the message.

### Hash

Hashing is the practice of mapping large data of variable size to small data of fixed size. The main purposes of a hash are summarizing data and comparing data.

#### Example

Renan is responsible for printing a contract (a one-page Word file) every time it changes, because it's a template used by his company's lawyers. So Renan generated a hash of that Word file's data, and instead of manually checking whether something changed in the file, he just generates a new hash and checks whether it's identical to the previous one.

Word file hash: 9f76d

Word file hash after a change: 8de3x

So if the Word file isn't changed, it will always have the same hash (summary), but once it has any change and a new hash is generated, it will be different from the previous one.

### Conclusion

These 2 concepts are widely used in tech, especially around security. If you're not in tech, it's worth knowing what each one is in simple terms, so you can start following what tech people are talking about. If you work in tech or are interested in the field, I think it's worth studying both concepts in more depth, along with the types of encryption and hashing, among other things.

### References
<https://viniciuscampitelli.com/slides/libsodium-php/#/2/1>
