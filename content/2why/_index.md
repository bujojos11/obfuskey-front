+++
title = "2Why?"
description = "Why do you need ObfusKey? Why was it made? This page explains the problems that ObfusKey solves by clearing the traditional hurdles about protecting your seedphrase from anyone accessing it or having it only in one place which can be a bigger problem than a solution regarding securing and ensuring your seedphrase will always be recoverable."
+++

## Why?

The point behind all this is to free yourself from the cold and impersonal yet very powerful set of random words that was given to you, exchanging it for something very personal yet inert and harmless that only you will be able to recover so you don't have to worry about storing it anymore.

## Why making ObfusKey?

As soon as I started to use cryptocurrencies and therefore wallets, I got worried about seedphrase storage. At first I just wrote them down on a piece of paper and hid the paper away. I was using various wallets like Metamask, Daedellus, Polkawallet, Electrum wallet, and right away the amount of papers I had to store started to become not only a logistical problem (where to put them, all in one place ? separated ? but then still need to know where they are and keep an eye on them etc..) but also a basic security problem that if anyone would find said papers, they would get access to my funds.

It felt paradoxical that the only way to safely store it is on a piece of paper which can be:
- found by anybody else than you, meaning loss of control over your wallet
- damaged/destroyed by environmental events (would it be fire, water, earthquake ...?)   
You can of course try to mitigate the second point by using a different media than paper, some might even use metal, but it doesn't help with the first point:   
*if anyone else than you finds your media, they get your keys, your cryptos.*

While this is a major issue with lightweight wallets, of course, in the case of an HD-wallet you could/should protect it with a passphrase BUT this doesn't solve the storage of the seedphrase. You shouldn't keep it public just because you used a passphrase since this passphrase can be brute-force and will be a single point of failure.

You can of course opt for a digital storage, which is a terrible idea for the following reasons:
  
### 1. Accessibility
If it is digital, it can be remotely:
- opened without leaving a trace
- copied without leaving a trace
- modified
- deleted


You can mitigate the first 3 by password protecting it but it won't help you if it is deleted. Also, if it is locally password-protected, it can be brute-forced. If it is remotely password protected (using 2FA and such) you can always get hacked/sim-swapped etc.
  
### 2. Digitality
The digitality itself can be more of a problem than a solution. If you want to securely store it digitally, you have to rely on encodings, cryptography, password protection etc which all make it impossible to store in any other form than digitally because, you can't print a password-protected zip-file. I mean, you could print out every byte of the file but typing it back will be quite something. And if you print it out as plain text you are back to square one with a piece of paper that anyone can find and can be destroyed. The inherent problem to the digital form is that it can only be digitally stored. 
  
### 3. Storage
If you rely on a text file inside of a zip file stored on a cloud service, you have to trust the cloud service to be there forever and never lose your file. In a funny twisted way, trying to self-custody your keys relying on some service to safe-guard your password-protected private-key should be seen as a third-party trust-based storage very similar to simply giving your keys to the service and letting it handle the safety (similarly to a crypto-exchange for example). If you must trust that a service/server will be up in order to get access to your seedphrase, therefore you are not totally in control of your seedphrase.
  
### 4. Security
Trying to break a password encryption is only a matter of computing power and can be performed fully offline. If the password is not found in usual password-listings, the attacker would have to run all possible character combinations. While it is not fast, the attacker will know they have broken the encryption because the text will be readable/the hash will match.
  
The main take-out is that to be perfectly safe you would need to have it both on a physical media AND under a digital form BUT without having to rely on any third party for the storage and protection of the file WHILE keeping the physical copy not readable.

The obvious solution to this problem is obfuscation for the following reasons:
- once obfuscated, it is useless unless you have the way to desobfuscate it so you can keep it under the digital form
- because it is an obfuscation within the mnemonic, it is still under the form of a seedphrase so it is easy to type, easy to print out so you can keep it physically
- but because it is under the form of a mnemonic phrase, it also means you can't just brute-force it back because you won't know if you successfuly broke it because the desobfuscation will always output a seemigly valid seedphrase. This will get clearer the further we go.
- if you use a passphrase-protected seedphrase, obfuscating your seedphrase makes it theoretically impossible to break without the password(s)


My first step was to switch position of a couple of words as a first-level of security, meaning anyone finding the paper could just end-up with an empty wallet and move on. But anybody really wanting to find my wallet for sure could simply jumble the words and see all the possible wallets and therefor gain access to my wallet.

Right away I knew there had to be a better way and decided to start working on a reversible procedural way of obfuscating my seedphrases rendering them completely unusable without the proper input.

## Why obfuscation over encryption?

When trying to make something secure, the usual way is to use encryption. Encryption is obviously safe, secure etc but I see two major drawbacks that are practically undeniable:
- encrypting a piece of text turns the original human readable text into another data form not easily human-readable, therefor not practical to write down and if needed, manually type back into a software
- an attacker knows when he broke the encryption by matching the hash or by turning the unreadable data into plain text.

These two reasons are why, in this case, obfuscation is far superior:
- When obfuscating plain text, the output is still plain text so you can easily manipulate this output to write it down on a piece of paper if that is what you choose to do. It does not force you into having your output under a digital form because the digital form forces you to copy/paste it in order to make use of it. Plain text data storage is far superior to  hashed data storage.
- When attempting to desobfucate, any input will give a seemingly correct output meaning you can't just compare two hashes, you actually have to perform a check on the data. In the case of seedphrases, you have to attempt to open a wallet and check the balance. Only then you can be sure if you do have the correct result.

## Why open-source it?

Because what is on the internet is most likely going to be there forever, the only way of making sure ObfusKey will always be available, would it be as an executable, as the source code of at least as the documentation, is to make it open-source and have people using it, playing with it, even integrating it in other projects if it is possible. This way, by distributing it, I know I will always be able to run it somehow. Of course, there are several github repositories and this website - which has a long lease on the domain name by the way - that are going to be around for a long time. On top of that, I can only encourage you to keep a version of the executable with any digitally stored obfuscated seedphrase you might have.


{{< paige/center >}}
Now, let's see [how it works](../3how).
{{< /paige/center >}}
