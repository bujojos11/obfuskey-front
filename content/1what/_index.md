+++
title = '1What?'
description = "What is Obfuskey? What is its purpose? What language is it written in? You will find all these information here."
+++

{{<paige/gallery align="center">}}
{{< paige/image alt="Text file resulting from an obfuscation after modifications with hints" src="obfuscation_example.png" >}}
{{</paige/gallery>}}

## What is ObfusKey?

ObfusKey is a revolutionary way of securing your cryptocurrency wallet's seedphrase that offers a complete shift of paradigm. It allows you to keep your seedphrase safe in multiple places and under multiple form, digital or physical, without having to be worried of someone else than you accessing it. It is a completely free, open source, rudimentary, offline and trustless solution to a decade old problem. It works with any wallet type on any blockchain and it not only is best suited to secure lightweight wallets (Metamask and other non-HD wallets) but also helps adding another security layer on top of your HD wallet's passphrase, if you happen to have one. 

## What is it, concretely?

ObfusKey is an open-source, very small piece of software that can be executed on most of the operating-systems (using ready-made executables) or on any machine where Python 3.11 is installed. It is fully offline and doesn't require any installation. If you decide to run the executable file you won't even need to install Python. It is not using any external library or dependencies and won't require anything outside of its own source code available in the github repo. 

If you wish to take a look at the complete documentation, please visit the [documentation page in the github repository](https://github.com/bujojo16/obfuskey/blob/master/Documentation/obfuskey.md)

## Open-source

Because you should never enter your seedphrase in a software that you can't trust and a big part of this trust is based on the source code being available for anybody to read.

## Python

Python was chosen for its simplicity. On a very high-level, Python strips away a lot of the complexity inherent to programming compared to other languages which is probably one of the reasons why so many people start learning to code using Python. This simplicity means that a lot of students and hobbyist are using Python but also that any seasonned programmer that has never seen a line of python code will be able to understand a Python source-code, given it was properly written.

Python is, in a way, very similar to the spoken language. If written in a clean and verbose way, even somebody with the bare minimum knowledge in programming will be able to understand what is the code doing. This is very important for this project because you should never execute a software you are not sure what is it doing.

## No external library

In order to really keep control over the complete code and avoid attacks that would be aimed at a dependency to corrupt ObfusKey, everything was written from scratch. For this reason the user-interface is what it is - a not very modern command-line UI. If the aesthetics were paramount, a graphical user interface could have been used but the main priority is security. By writing everything from scratch and keeping it simple, it is easier for anybody to read the intirety of the source code and the project is not at risk of somebody inserting malicious code in an external library the project would be using.


{{< paige/center >}}

Up next: [Why?](../2why)

{{< /paige/center >}}
