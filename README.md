# create-ssh-key
create ssh-key

## generate new ssh key

`ssh-keygen -t ed25519 -C "your_email@example.com`
### or
`ssh-keygen -t rsa -b 4096 -C "your_email@example.com`

 ## adding ssh-key to the ssh-agent

`eval "$(ssh-agent -s)"`
### may need to use

`exec ssh-agent bash` or `exec ssh-agent zsh`


`ssh-add ~/.ssh/id_ed25519`

### copy ssh-key to your app

`xclip -sel clip < ~/.ssh/id_rsa.pub`