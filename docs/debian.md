# Debian


## Init

```
sudo apt-get update && sudo apt-get install git vim vnstat tmux nscd  sudo net-tools zsh
```


#### hostname

```
sudo hostnamectl set-hostname host.example.com
```


####  Install zsh
```
sudo apt-get install zsh git wget
```

#### Install oh-my-zsh
```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

chsh -s /bin/zsh
```



## BBR

#### Add
vim `/etc/sysctl.conf` Add:

```
net.core.default_qdisc=fq 
net.ipv4.tcp_congestion_control=bbr 
```

#### Reload

```
sudo sysctl -p
sudo sysctl net.ipv4.tcp_available_congestion_control
sudo lsmod | grep bbr
```



