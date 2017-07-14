# Guest Addon

RHEL7でファイル共有が上手く行かない。以下で解決。(VirtualBoxは4.3.12)

* /usr/include/linux/version.h　をコピー
* 以下のソース変更

```
vi /opt/VBoxGuesstAdditions-4.3.12/src/vboxguest-4.3.12/vboxguest/r0drv/linux/memobj-r0drv-linux.c

### 1536, 1541行目
KERNEL_VERSION(3, 13, 0) を KERNEL_VERSION(3, 10, 0)に変更
```
* `/etc/init.d/vboxadd setup`
* `mount -t vboxsf 共有名 マウント先ディレクトリ`

参考) https://motherfuckerblog.wordpress.com/2014/09/06/centos7%E3%82%92virtualbox%E3%81%A7/
