# proxmox pt3

After getting wireguard split tunnel and ssh access to the server, we are ready to install vms.

First problem was, none of the bigger drives are seen on the proxmox.

![](assets/1743832889590.png)

Looking if they are actually seen at all, i can find them here: 

![](assets/1743832988279.png)

Learning that if not using the dell hardware raid system, the next best practice is to use ZFS with mirror setup

We are going with  sda+sdb mirrored by sdc+sdd and sde as spare if one drive fails

cleaning old partitions
```
for disk in sda sdb sdc sdd sde; do
  wipefs -a /dev/$disk
done
```

creating our preferred mirror setup and verifying
```
zpool create zfs-vmlab mirror sda sdb mirror sdc sdd spare sde
```

![](assets/1743834163948.png)

we still have an nvme to use, now configuring them to do caching and logs

`cfdisk /dev/nvme0n1`

![](assets/1743834762080.png)

![](assets/1743834892312.png)

```
zpool add zfs-vmlab log /dev/nvme0n1p1
zpool add zfs-vmlab cache /dev/nvme0n1p2
```

![](assets/1743835068905.png)

now adding the newly created partitions to proxmox

![](assets/1743835234910.png)

datacenter -> storage -> add -> ZFS

noticed cant add iso store, so adding a dataset for the images

`zfs create zfs-vmlab/iso-store`

now returning to add zfs, we can see iso-store also-

but we go add -> directory

![](assets/1743835683820.png)

and then add ZFS

---

now getting iso images for vms

![](assets/1743837537060.png)

spending lots of time trying to find some good windows iso images, but seems they try to hide them all behind the "windows download tool/ installer"

finally found some images we can start testing with:

![](assets/1743926118906.png)

also corrected the dir, by mistake first downloaded into /mnt/iso-store/ but correct path was /mnt/iso-store/template/iso/
