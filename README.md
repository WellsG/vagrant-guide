# vagrant-guide (maitai2)

### Vagrant box

https://atlas.hashicorp.com/boxes/search?utm_source=vagrantcloud.com&vagrantcloud=1

### How to package custom box
```
$ vagrant up
$ vagrant ssh
$ cat /dev/zero > zero.fill;sync;sleep 1;sync;rm -f zero.fill
$ exit
$ vagrant package --output ~/Documents/maitai2.box
```

:point_right: Ref: Making smaller base boxes
https://github.com/mitchellh/vagrant/issues/343

### Add custom box 
```
$ vagrant box add ~/Documents/maitai2.box --name maitai2
```

### Init 
```
$ vagrant init maitai2
$ vagrant up --provider virtualbox
$ vagrant ssh
```
### Note:  If you want to support synced folder, please install the following extra plugin:
```
config.vm.synced_folder "/home/wguo/vagrant/workspace", "/home/wguo/vagarant_data", owner: "wguo", group:"wguo", create:true
```
```
[~/vagrant] $ vagrant plugin install vagrant-vbguest
```

