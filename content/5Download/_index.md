+++
title = "5Download"
description = "Downloading ObfusKey. Do you want to download the whole project or just an executable file?"
[paige.alert]
message = "Don't forget to visit the \"Support the Project\" page to help the project!"
type = "primary"
+++

As explained in the previous section, you can either download the whole project or just the executable fitting your operating system.

## Whole Python project

It is strongly recommended to download the whole project, read the source code and then either run it with Python 3.11 or making your own executable using PyInstaller.

[ObfusKey github repository](https://www.github.com/bujojo16/obfuskey)

## Executables

If you want to simply use executables, this is also possible. For safety, you should always check the sha256 hash of the executable file. It should be matching the one mentioned here. Since this website and the repository are completely isolated from each-other, hacking both is very unlikely. If safety is really what you are looking for, then you should download the whole project, read the code and then execute it from the code.

["ObfusKey_executables" github repository](https://www.github.com/bujojo16/obfuskey_executables)

You should download the whole project from the repository so you already have the file structure with the default mnemonic (BIP-39 English) in the correct directory. The hash that matters is the hash of the executable file, not the zip file.

{{< paige/tabs >}}
{{< paige/tabs/buttons >}}
{{< paige/tabs/button >}}Windows{{< /paige/tabs/button >}}
{{< paige/tabs/button >}}Linux{{< /paige/tabs/button >}}
{{< /paige/tabs/buttons >}}
{{< paige/tabs/panes >}}
{{< paige/tabs/pane >}}
Sha256 hash of "obfuskey-2.1.exe"   
2f7644180e7e9655e9d8af1f8a8be90ea382858a94e24f5285f3bd58bfbe334b
{{< /paige/tabs/pane >}}
{{< paige/tabs/pane >}}
Sha256 hash of "ofbuskey-2.1_linux"   
b92338922440cd6dd6ed58d1987024502163d6666d7803d32b44fec88522bca6
{{< /paige/tabs/pane >}}
{{< /paige/tabs/panes >}}
{{< /paige/tabs >}}

Because of the automated testing running when executing these files, you will have to keep the file structure with the mnemonic file's location in order to run the executables. Otherwise, they will crash.

## Direct zip-archive download

If for any reason you feel comfortable to do so, you can download the executable-zip package from here. Keep in mind that if you do, you should still check the sha256 hashes but this time compare it to the one mentioned in the github repository since, as said before, this website and the repos are completely isolated from each other and therefore they should always be matching to insure no hack has happened.
 
Anyhow, by clicking the link below you will download the executable package which contains the executable files for both Linux and Windows as well as the default mnemonic.

[obfuskey_executables-main.zip](../obfuskey_executables-main.zip)

{{< paige/center >}}
If you wish to show some gratitude and [support the project, it's here!](../6supporttheproject)
{{< /paige/center >}}
