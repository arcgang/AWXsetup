# AWXsetup

## Installation pre-reqs
``` sh
sudo yum -y install git gcc gcc-c++ nodejs gettextdevice-mapper-persistent-data ivm2 bzip2 python3-pip
```
## install docker ce 
``` sh
sudo amazon-linux-extras install docker
sudo service docker start
sudo usermod -a -G docker ec2-user
```
Make docker auto-start
``` sh
sudo chkconfig docker on
```

Reboot to verify it all loads fine on its own.
``` sh
sudo reboot
```



