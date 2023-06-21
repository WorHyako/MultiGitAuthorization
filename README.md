# Multiple Git authorization via ssh

## Preliminary actions

Generate ssh key by:

```shell
ssh-keygen
```

Ssh agent will ask u to choose ssh-key path and name:  
`Enter file in which to save the key (C:\Users\username\.ssh/key-name)`

Password may be passed. Just double Enter next part:  
`Enter passphrase (empty for no passphrase):`

Ssh-agent will generate public and private part of ssh-key. In GitHub/GitLab setting add new ssh-key(public part) in
trust list.

---

## Config filling

In .ssh folder create __[config](.ssh/config)__ file without extension and write config data: server, port, username
& etc.

List of options and description you can read on
[ssh.com](https://www.ssh.com/academy/ssh/config#:~:text=The%20ssh%20program%20on%20a,ssh%2Fconfig%20is%20used%20next.)  

---

## Config using

For example, you configured __[config](config-example)__  
So let's try clone some git repos and start with personal account

```shell
git clone git@github-self:User/RepoName.git
```

Git will ask u for trusting remote server and using your ssh key:  
`Are you sure you want to continue connecting (yes/no/[fingerprint])?`  
U can check destination end point and ssh key type etc.  
In case of consent this pair of host and ssh key will be added to __[known_hosts](.ssh/known_hosts)__ file. 
This file will be created automatically 

Now let's copy with work account

```shell
git clone git@gitlab-work:Organization/RepoName.git
```

Git again ask u about a pair of host and ssh key. Check it if you want and continue

---

- Hope the community will help me write correct script(.bat/.sh) file or ssh config. This repo is fast solution to solve
  the problem of automation and comfort.

- Tested on macOS & Windows
