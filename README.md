kscripts
========

Some simple scripts to help with compiling kernel modules against different kernel versions.

kaddmod:
Checks if kernel version is present. If not, fetch kernel version, build for UML.
Then it compiles the kernel module against this kernel version, mounts the UML image and
rsyncs the specified directory containing the LKM onto it, and unmounts the image and boots UML.

kfix/kmake:
Fetch/build kernel version. Called from kaddmod.

uml:
Simple wrapper for UML. To be ran from a kernels root directory after it was built for UML. Also called from kaddmod.
