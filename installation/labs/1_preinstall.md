# Prerequisites output

```
[root@ip-172-31-5-113 ~]# echo 1 > /proc/sys/vm/swappiness
[root@ip-172-31-5-113 ~]# sudo cat /proc/sys/vm/swappiness
1
[root@ip-172-31-5-113 ~]# vim /etc/fstab
[root@ip-172-31-5-113 ~]#
[root@ip-172-31-5-113 ~]#
[root@ip-172-31-5-113 ~]# lsblk
NAME    MAJ:MIN RM  SIZE RO TYPE MOUNTPOINT
xvdf    202:80   0  100G  0 disk
└─xvdf1 202:81   0    8G  0 part
xvde    202:64   0    8G  0 disk /
[root@ip-172-31-5-113 ~]#
[root@ip-172-31-5-113 ~]# mkfs.ext4 /dev/xvdf
[root@ip-172-31-5-113 ~]#
[root@ip-172-31-5-113 ~]# sudo cat /etc/fstab
LABEL=centos_root               /        ext4      defaults         0 0
devpts     /dev/pts  devpts  gid=5,mode=620   0 0
tmpfs      /dev/shm  tmpfs   defaults         0 0
proc       /proc     proc    defaults         0 0
sysfs      /sys      sysfs   defaults         0 0
/dev/xvdf /opt/cloudera ext4 defaults,noatime 0 0

[root@ip-172-31-5-113 ~]# mount -a

[root@ip-172-31-5-113 ~]# sudo sysctl -a | grep hugepage
vm.nr_hugepages = 0
vm.nr_hugepages_mempolicy = 0
vm.hugepages_treat_as_movable = 0
vm.nr_overcommit_hugepages = 0
[root@ip-172-31-5-113 ~]#
[root@ip-172-31-5-113 ~]# sudo tune2fs -l /dev/xvdf
tune2fs 1.41.12 (17-May-2010)
Filesystem volume name:   <none>
Last mounted on:          <not available>
Filesystem UUID:          f5676592-5d96-4f8b-9b91-2068edffd35c
Filesystem magic number:  0xEF53
Filesystem revision #:    1 (dynamic)
Filesystem features:      has_journal ext_attr resize_inode dir_index filetype needs_recovery extent flex_bg sparse_super large_file huge_file uninit_bg dir_nlink extra_isize
Filesystem flags:         signed_directory_hash
Default mount options:    (none)
Filesystem state:         clean
Errors behavior:          Continue
Filesystem OS type:       Linux
Inode count:              6553600
Block count:              26214400
Reserved block count:     1310720
Free blocks:              25755051
Free inodes:              6553589
First block:              0
Block size:               4096
Fragment size:            4096
Reserved GDT blocks:      1017
Blocks per group:         32768
Fragments per group:      32768
Inodes per group:         8192
Inode blocks per group:   512
Flex block group size:    16
Filesystem created:       Mon Jun  5 14:54:11 2017
Last mount time:          Mon Jun  5 14:58:53 2017
Last write time:          Mon Jun  5 14:58:53 2017
Mount count:              1
Maximum mount count:      27
Last checked:             Mon Jun  5 14:54:11 2017
Check interval:           15552000 (6 months)
Next check after:         Sat Dec  2 14:54:11 2017
Lifetime writes:          1733 MB
Reserved blocks uid:      0 (user root)
Reserved blocks gid:      0 (group root)
First inode:              11
Inode size:               256
Required extra isize:     28
Desired extra isize:      28
Journal inode:            8
Default directory hash:   half_md4
Directory Hash Seed:      137632e6-79ee-4cd2-b07e-bb09c36f6dae
Journal backup:           inode blocks
[root@ip-172-31-5-113 ~]#
[root@ip-172-31-5-113 ~]# cat /etc/sysconfig/network
NETWORKING=yes
NETWORKING_IPV6=no
HOSTNAME=localhost.localdomain
[root@ip-172-31-5-113 ~]#
[root@ip-172-31-5-113 ~]#
[root@ip-172-31-5-113 ~]# service nscd status
nscd (pid 4986) is running...
[root@ip-172-31-5-113 ~]# service ntpd status
ntpd (pid  5014) is running...
```

