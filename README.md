# Multi Git authorization via ssh

#### via Windows

> ## Preliminary actions
> Generate ssh key via PowerShell or CMD by
>
> _$ ssh-keygen_
>
> Ssh agent will ask u to choose ssh-key path and name
>
> _$ Enter file in which to save the key (C:\Users\username\.ssh/key-name)_
>
> Password may be passed. Just double Enter next part
>
> _$ Enter passphrase (empty for no passphrase):_
>
> Ssh-agent will generate public and private part of ssh-key. In GitHub/GitLab setting add new ssh-key(public part) in
> trust list

> ## Config filling
> In .ssh folder create _[config](.ssh/config)_ file without extension and write config data: server, port, username
> & etc
