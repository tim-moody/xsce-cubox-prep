xsce-cubox-prep
===============

Here are some scripts and images to create a cubox install ready for xsce

Scripts:

These go in /root/xsce-prep

xsce-prepdisk - formats an external hdd and copies a rootfs image to it 
                 and sets up bind mounting

fstab.in      - mounting definitions for fstab
fstab.ORIG    - the original fstab

extmnt        - is copied to /etc/rc.d/init.d to do some mounts that
                don't work in fstab and some housekeeping
              - reverts to the original fstab if the hdd is not attached
                because otherwise networking and other things break.
                
xsce-hddctl   - a utility to enable and disable access to the external hdd

Images:

The rootfs image also belongs in /root/xsce-prep and gets copied to /dev/sda3