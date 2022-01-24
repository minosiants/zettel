202111171059
Tags: #cli #linux
__
# Storage Devices
`mount` - moun device  
`umount` - unmount device  
`fsck` - check and restore file systems  
`fdisk` - working with devices table  
`mkfs` - create file systems  
`dd`  - bock recordes stright to device  
`genisoimage` (` mkisofs`) - creat file image iso 9660  
`wodim` (`cdrecord`) - record data to optical device `md5sum` - md5   

`/etc/fstab`  - file system table  


### names of storage devices 
`/dev/fd*`- floppy disks  
`/dev/hd*` - IDE (PTA)  
`/dev/lp*` - printers   
`/dev/sd*` - SCSI  
`/dev/sr*` - CD/DVD  

`sudo umount /dev/sdb1` 
`sudo fdisk /dev/sdb` - format partition
`m` - show help for above command  

`sudo mkfs -t ext4 /dev/sdb1` - create ext4 filesystem  

`sudo fsck /dev/sdb1` - file system check  

`dd` - data fefinition used to move data  

`dd if=/dev/sdb of=/dev/sdc`   
`dd if=/dev/cdrom of=ubuntu.iso` make copy of cdrom to file  
`genisoimage -o cd-rom.iso -R -J ~/cd-rom-files`  copy files into iso  

`mkdir /mnt/iso_image`  
`mount -t iso9660 -o loop image.iso /mnt/iso_image`  - mount iso file into file system  

`wodim dev=/dev/cdrw blank=fast` - before burning cdrw it should be cleaned   
`wodim dev=/dev/cdrw image.iso` - birning image  













 
 