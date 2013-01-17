VBoxManage createhd --filename /Volumes/data/vm/rsms/rsms-extra.vmdk --size 81920 --format VMDK
http://www.perkin.org.uk/posts/create-virtualbox-vm-from-the-command-line.html

VBoxManage storageattach rsms --storagectl "IDE Controller" --port 0 --device 1 --type hdd --medium /Volumes/data/vm/rsms/rsms-extra.vmdk

http://www.tutonics.com/2012/11/ubuntu-lvm-guide-part-1.html

merging snapshots int one vdi - 
http://www.brightavenue.com/blog/2011/cloning-from-virtualbox-vdi-snapshots/
VBoxManage clonehd rsms.vdi rsms-full.vdi
VBoxManage clonehd rsms/Snapshots/\{9e045506-315a-4a42-9321-5b6639699c80\}.vdi rsms-full.vdi --existing
