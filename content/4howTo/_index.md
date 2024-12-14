+++
title = "4How To?"
+++

## How to use it?

When running ObfusKey you will always have extensive help menus and descriptions of what is going on and what to do but here is a quick summary of what will happen after you downloaded it and installed it.

1. Automated tests
In order to make sure you are not using a corrupted version of obfuskey, there are end-to-end tests running at every launch of the software. This test will run a basic obfuscation-desobfuscation cycle of a known seedphrase and its results and compare them. If anything goes wrong, the software will crash and you won't be able to continue
2. Menus
If you can see the menu, this means the tests ran normally. In order to interact with the interface, you have to enter the character of the options you want to use in the menu and press enter.
3. You should only use the latest version of Obfuskey since the first iteration is obsolete. This 1.0 version was only released for a short while and most probably nobody ever used it but I decided to always keep all versions (if I ever make newer ones) directly in the software so it is always possible to recover obfuscated seedphrases.
4. Mnemonic selection
You will first have to select which mnemonic your seedphrase is using. The default mnemonic coming with Obfuskey is the english BIP-39 mnemonic. If you wish to use a different one, you can manually add it to the "Mnemonics" directory. Obfuskey will always check your seedphrase is found in the mnemonic and won't let you run something impossible.
5. Seedphrase
You will then be prompted to enter the words of your seedphrase, in the correct order, one by one. There are no limitation on the length of the seedphrase. When you are done, just press enter without adding any word. You will then be asked to double check you entered the correct seedphrase.
6. Passwords
After that you will be asked to enter as many passwords as you desire. Every password adds another layer of obfuscation. You should read the documentation regarding passwords.
7. Obfuscation or Desobfuscation
You can then choose do you want to perform an obfuscation of your seedphrase or a desobfuscation. If you have entered your original seedphrase, perform an obfuscation. An automated desobfuscation test will be run to verify you can actually retrieve your seedphrase using the passwords provided. This is only to for peace of mind. If you want to run a desobfuscation of your newly obfuscated seedphrase, you will have to return to the seedphrase menu to enter the obfuscated seedphrase and then run the desobfuscation.
8. File saving
The outcome of your obfuscation will then be saved into a text file located in \<FIX ME\>. You have to open this file with a text editor and replace characters of your passwords with stars in order to make it safe. You also should write some hints regarding each password so your future self can remember the passwords easily. Make sure to be as cryptic as possible but still clear enough to yourself.

When exiting obfuskey, this is it. There is no storage of any of the data processed, not the passwords nor the seedphrase. It is recommended to then manually run a desobfuscation and see if you feel comfortable with destroying your seedphrase paper.

I recommend sending this obfuscation text-file to your email address, store it on your hard drive, write it down on several different medias, since it is now safe to store. 

## How to run it?

In this section you will find different methods of executing ObfusKey and how to use it.

Bit of a foreword:
Before entering your seedphrase for obfuscation, you should definitely run several try outs with random seedphrases to see if this is the solution you need. You can run it in a virtual machine and even disconnect your internet connection, Obfuskey is fully local and doesn't call or run any outside code, doesn't require any other software. In fact, the safest way of using it would be on Tails Os.

First, you need to choose how do you want to be able to execute the software. Do you want to keep it simple and just have an executable file to run ? Do you want to run it with Python ? Or do you want to make your own executable so you can be sure of what you are compiling ?

### Least safe method: download the executable

Because the main goal of ObfusKey is to be easy to run by anybody with a computer, there is a possibility of downloading an executable for your operating system and just running it. However, because you should never run a software you don't trust and obviously I am not Microsoft or Apple or any big tech company, you shouldn't run this without taking some level of precautions.

1. Download the file directly from the github repository   
By doing this, you can be sure you are downloading the latest official version and you can already heavily reduce the risks involved. Make sure to check if there was any recent commit to the project and if so, take a moment to check what was in the commit(s).


2. Compare the hash of the file   
This is not a perfect method but it adds a level of certainty in that you can be sure you are running the official version.
To get the hash of any file in Linux or Windows, just open a terminal (Windows, search: "cmd" | Linux, search for "Terminal"), use the command "cd \<name of directory\>" to change directory (using Tab will display possible directories) and get to the location of the file, then using :

- Windows:   
{{< paige/code >}}
certutil -hashfile <name-of-file-with-extension> -sha256
{{< /paige/code >}}

- Linux:   
{{< paige/code >}}
sha256sum <name-of-file-with-extension>
{{< /paige/code >}}

you will get the sha256 hash of the file that you can compare with the one mentioned in the README (also visible in the github page). If this hash doesn't match, you should delete this file and definitely not try to run it.

### Safer method: run in python

Once you have read the source code, after cloning the git repo, simply executing "python main.py" will let you run the software.   
Please, do note that only Python3, version 3.11 or above, will run the project.

### Safest method: make your own executable for Tails/Qubes Os

Because we are talking about securing your cryptocurrency wallets, ObfusKey was designed to run on safe OS. To reduce all risks of someone spying on you while using it, it is strongly recommended to run it in Tails Os. The safest way would be that you would yourself compile your own executable file and then run it in Tails Os but if you want you can also use the compiled versions for Linux on the repo. Always remember to check the sha256 hash of the file for safety.

{{< paige/center >}}
Follow this link for [all available download method](../5download)
{{< /paige/center >}}
