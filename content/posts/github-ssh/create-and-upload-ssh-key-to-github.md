---
title: "Create and Upload an SSH Key to Github"
date: 2022-12-12T19:56:15-0800
description: Create and Upload an SSH Key to Github
menu:
  sidebar:
    name: Create and Upload an SSH Key to Github
    identifier: sshkey-and-github
    weight: 10
tags: ["SSH", "Github"]
categories: ["Basic"]
---
To generate an SSH key and upload it to GitHub, follow these steps:
1.  Open a terminal on your computer and run the following command:
```bash
ssh-keygen -t ed25519 -b 512
```
2.  When prompted, enter a file in which to save the key. You can press Enter to accept the default file location.
3.  Next, you will be asked to enter a passphrase for the key. This is an optional security measure that adds an extra layer of protection to your key. If you choose to set a passphrase, you will be required to enter it every time you use the key.
4.  After the key has been generated, run the following command to print the key to your terminal:
```bash
cat ~/.ssh/id_ed25519.pub
``` 
1.  This will print the key to your terminal. You can now copy the key by highlighting it with your mouse and pressing Ctrl+C (or Cmd+C on macOS).
2.  In your web browser, go to the GitHub website and log in to your account.
3.  Click on your profile picture in the top right corner of the page and select Settings from the drop-down menu.
{{< img src="/posts/github-ssh/github-settings.png" width="200" align="center" title="Github Settings" >}}
4.  In the Settings menu, navigate to the SSH and GPG keys section and click on the New SSH key button.
{{< img src="/posts/github-ssh/github-new-key.png" align="center" title="Github Settings" >}}
5.  In the "Title" field, enter a name for the key that will help you identify it later (for example, "My laptop").
6.  Paste the key that you copied in step 5 into the "Key" field.
7.  Click on the Add SSH key button to save the key to your GitHub account.

You should now be able to use the key to authenticate with GitHub. For more information on using SSH keys with GitHub, you can refer to GitHub's [documentation](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account).
