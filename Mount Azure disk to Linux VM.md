# Mount Azure disk to Linux VM
https://learn.microsoft.com/en-us/azure/virtual-machines/linux/attach-disk-portal
https://acloudguru.com/hands-on-labs/attaching-an-azure-managed-disk-to-a-linux-vm

1. `lsblk` zjistit, kterej disk nemám připojenej.
```
NAME    MAJ:MIN RM  SIZE RO TYPE MOUNTPOINT
loop0     7:0    0 67.8M  1 loop /snap/lxd/22753
loop1     7:1    0 63.2M  1 loop /snap/core20/1623
loop2     7:2    0   48M  1 loop /snap/snapd/17029
sda       8:0    0   30G  0 disk
├─sda1    8:1    0 29.9G  0 part /
├─sda14   8:14   0    4M  0 part
└─sda15   8:15   0  106M  0 part /boot/efi
sdb       8:16   0   32G  0 disk
└─sdb1    8:17   0   32G  0 part /mnt
sdc       8:32   0  256G  0 disk
sr0      11:0    1  628K  0 rom
```
2. Nepřipojenej je disk **sdc**.
3. Je potřeba disk připravit: `sudo fdisk /dev/sdc`
```
Command (m for help): n
Partition type
   p   primary (0 primary, 0 extended, 4 free)
   e   extended (container for logical partitions)
Select (default p): p
Partition number (1-4, default 1): 1
First sector (2048-536870911, default 2048):
Last sector, +/-sectors or +/-size{K,M,G,T,P} (2048-536870911, default 536870911):

Created a new partition 1 of type 'Linux' and of size 256 GiB.

Command (m for help): w
The partition table has been altered.
Calling ioctl() to re-read partition table.
Syncing disks.
```
4. Kouknu na `lsblk` a vidím, že už je to lepší.
```
sdc       8:32   0  256G  0 disk
└─sdc1    8:33   0  256G  0 part
```
5. Naformátuju novej disk `sudo mkfs -t ext4 /dev/sdc1`
6. Vytvořím si adresář, kam disk namontuju `sudo mkdir /datadrive`
7. Můžu disk rovnou namontovat `sudo mount /dev/sdc1 /datadrive`
8. Zjistím si UUID disku `sudo -i blkid | grep sdc1`
```
/dev/sdc1: UUID="b3674c3c-3d79-4478-b1e0-0e8c670657f6" TYPE="ext4" PARTUUID="440497c7-01"
```
9. Musím ještě upravit fstab, aby se mi disk montoval vždycky, `sudo vi /etc/fstab`
10. Do **fstab** přidat záznam
```
UUID=b3674c3c-3d79-4478-b1e0-0e8c670657f6   /datadrive   ext4   defaults   1   2
```
11. Otestovat správné namontování lze pomocí
```
# sudo umount /datadrive
# sudo mount /datadrive
```
12. Nebo se dá domontovat všechno zaráz reloadem fstab `sudo mount -a`
13. Velikost aktuálního adresáře si zobrazím `du -hs .`, když tam nedám to `s`, tak to mám i s podadresářema.