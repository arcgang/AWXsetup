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

## docker-compose install

``` sh
sudo curl -L https://github.com/docker/compose/releases/download/1.22.0/docker-compose-$(uname -s)-$(uname -m) -o /usr/local/bin/docker-compose
```

NOTE: to get the latest version (thanks @spodnet): 
``` sh 
sudo curl -L https://github.com/docker/compose/releases/latest/download/docker-compose-$(uname -s)-$(uname -m) -o /usr/local/bin/docker-compose
```


Fix permissions after download:
``` sh
sudo chmod +x /usr/local/bin/docker-compose
```

Verify success:

``` sh
docker-compose version
```
