# Multiple Git authorization via ssh

#### via Windows

> ## Preliminary actions
> Generate ssh key via PowerShell or CMD by:
>
> _$ ssh-keygen_
>
> Ssh agent will ask u to choose ssh-key path and name:
>
> _$ Enter file in which to save the key (C:\Users\username\.ssh/key-name)_
>
> Password may be passed. Just double Enter next part:
>
> _$ Enter passphrase (empty for no passphrase):_
>
> Ssh-agent will generate public and private part of ssh-key. In GitHub/GitLab setting add new ssh-key(public part) in
> trust list.

> ## Config filling
> In .ssh folder create _[config](.ssh/config)_ file without extension and write config data: server, port, username
> & etc.

> ## Using multiple git accounts
> Fill both _[first](first-acc.bat)_, _[second](second-acc.bat)_ etc .bat files to required name/email. Move it to
> Desktop location as an example of convenient location. Run these .bat files to switch git accounts, because otherwise
> commits will be signed with default global username.

- Hope the community will help me write correct script(.bat/.sh) file or ssh config. This repo is fast solution to solve
  the problem of automation and comfort.
