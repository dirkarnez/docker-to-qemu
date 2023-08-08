docker save -o image.tar image-name:tag
qemu-img convert -f raw -O qcow2 rootfs.img vm-disk.qcow2
qemu-system-x86_64 -m 2G -hda vm-disk.qcow2 -boot c -nographic
