# https://askubuntu.com/questions/157793/why-is-swap-being-used-even-though-i-have-plenty-of-free-ram

What to do :
0/ check currently swap configuration (result with problems should be by default 60)
``cat /proc/sys/vm/swappiness``

1/ remove currently swapped data :
``sudo swapoff -a``

2/ change permanent configuration for swapiness :
``sudo vim /etc/sysctl.conf``
if `vm.swappiness` value does not exists, add at the bottom of file `vm.swappiness = 10`, else update value to `10`

3/ apply changes right now
``sudo sysctl --load=/etc/sysctl.conf``

4/ check changes are applied
``cat /proc/sys/vm/swappiness``
Should return `10`

System should not over swap right now !
