# Raspberry Pi 4

## Install
### OS
https://www.raspberrypi.org/software/

##### ssh
https://www.raspberrypi.org/documentation/remote-access/ssh/
```
$ sudo raspi-config
>>> Select 'Interfacing Options'
```

##### git
```
$ git config --global user.email "you@example.com"
$ git config --global user.name "my name"
```
##### alias
https://www.raspberrypi.org/documentation/linux/usage/bashrc.md
```
$ cp .bash_aliases ~/.bash_aliases
```

### MariaDB
https://pimylifeup.com/raspberry-pi-mysql/
##### Enable remote connection
https://howtoraspberrypi.com/enable-mysql-remote-connection-raspberry-pi/

### Jupyter notebook
https://www.instructables.com/Jupyter-Notebook-on-Raspberry-Pi/
```
## example
$ nohup jupyter-notebook --ip="192.168.0.11" --no-browser &
```

### fancontrol
https://gyuha.tistory.com/506
