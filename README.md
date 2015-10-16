### System Info
#### CentOS 7.0

#### Setup
```
git clone git@github.com:Ineeza/centos_vm.git
cd centos_vm
vagrant up
```

##### Configure Firewall for using port 3000 (WEBrick default)
```
sudo su
firewall-cmd --add-port=3000/tcp --zone=public --permanent
```

##### Create project and start it
```
rails new hoge
cd hoge
rails s -b 0.0.0.0
```

##### Open your browser and visit the following address
```
127.0.0.1:3000
```
