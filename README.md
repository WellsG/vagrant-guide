# vagrant-guide

### how to package custom box
```
vagrant up
vagrant ssh
cat /dev/zero > zero.fill;sync;sleep 1;sync;rm -f zero.fill
exit
vagrant package --output ~/Documents/maitai2.box
```
