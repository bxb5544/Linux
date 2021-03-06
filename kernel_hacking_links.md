## Kernel hacking links ((WIP))
A mess of links that have been helpful to me, adding them as I find them.  Hopefully this will save some people a lot of time on Google :) 
I'll try to organize them by topic as best as I can, and eventually add a table of contents.
These links assume that you're already comfortable in a *NIX environment and know your way around as a GNU/Linux user, i.e. shell commands & compiling your own kernels.
Also, it should be assumed for most stuff that the first place to look is the source code.

#### Books
- My 2 holy grails:
  - https://lwn.net/Kernel/LDD3/
  - https://www.amazon.com/Linux-Kernel-Development-Robert-Love/dp/0672329468
 - 
 
#### C standards, asm, & compiler stuff
- http://www.iso-9899.info/wiki/The_Standard
- https://gcc.gnu.org/wiki/ListOfCompilerBooks
- https://gcc.gnu.org/onlinedocs/
- https://clang.llvm.org/docs/index.html
- https://www.intel.com/content/dam/www/public/us/en/documents/manuals/64-ia-32-architectures-software-developer-instruction-set-reference-manual-325383.pdf
- Arm
  - "Arm basics" notes https://bbchannel.dev/2020/10/arm-basics/
  - https://developer.arm.com/architectures/instruction-sets
- https://riscv.org/specifications/isa-spec-pdf/
 
#### Getting started: first patches, coding style, & LKML etiquette
- https://kernelnewbies.org/
  - A plethora of resources, taking the time to check out what they have to offer is worth it. 
- https://www.kernel.org/doc/html/latest/process/submitting-patches.html
- https://www.kernel.org/doc/html/latest/process/email-clients.html
- https://www.kernel.org/doc/html/latest/process/coding-style.html
- http://tuxdiary.com/2015/03/22/check-kernel-code-checkpatch/
- https://www.kernel.org/doc/html/latest/kbuild/index.html
  - All about compiling kernels, from kconfig to Makefiles, GCC to Clang.
- https://lore.kernel.org/lkml/

#### Git
- https://kernelnewbies.org/OutreachyRebase
- https://www.kernel.org/doc/html/latest/maintainer/rebasing-and-merging.html
- https://git-scm.com/book/en/v2/Git-Branching-Rebasing

#### Work environment
- http://cscope.sourceforge.net/cscope_vim_tutorial.html
- https://medium.com/code-dementia/how-cscope-makes-my-life-easier-6a0f13ca79e6
- https://linuxcontainers.org/
  - LXC/LXD has been invaluable for keeping my workspace clean & also having different toolchain environments at my disposal for building old kernels (and old AOSP versions)

#### Kernels
- linux-next
  - https://www.kernel.org/doc/man-pages/linux-next.html
  - https://www.man7.org/linux/man-pages/man8/debugfs.8.html
  - https://www.kernel.org/doc/html/latest/filesystems/debugfs.html

#### Debugging
- https://static.lwn.net/images/pdf/LDD3/ch04.pdf
- https://d3s.mff.cuni.cz/files/teaching/nswi161/slides/06_debugging.pdf
- Oops & panics
  - http://www.gonehiking.org/ShuahLinuxBlogs/blog/2018/10/21/the-linux-kernel-has-bugs-really/
  - https://sanjeev1sharma.wordpress.com/tag/debug-kernel-panics/
  - https://www.opensourceforu.com/2011/01/understanding-a-kernel-oops/
  - http://neependra.net/kernel/Debugging_Kernel_OOPs_FUDCon2011.pdf
  - https://www.kernel.org/doc/html/latest/admin-guide/bug-hunting.html
  - https://lwn.net/Articles/592724/ (decode_stacktrace)
  - https://blog.seibert-media.com/2018/01/04/log-book-linux-cpu-lockups/
  - http://www.inetservicescloud.com/knowledgebase/what-is-a-cpu-soft-lockup/
 - Tools
    - https://www.kernel.org/doc/html/latest/dev-tools/gdb-kernel-debugging.html
    - https://linux.die.net/man/1/objdump
 - KASAN
    - https://www.kernel.org/doc/html/latest/dev-tools/kasan.html?highlight=kasan
    - https://lwn.net/Articles/618180/
    - https://events.static.linuxfound.org/sites/events/files/slides/LinuxCon%20North%20America%202015%20KernelAddressSanitizer.pdf
    - https://patchwork.kernel.org/cover/10579913/
    - https://blog.fuzzing-project.org/23-Kernel-Address-Sanitizer-KASAN.html
    - https://cwe.mitre.org/data/definitions/416.html
    - https://securityintelligence.com/use-after-frees-that-pointer-may-be-pointing-to-something-bad/

#### Module basics
- https://static.lwn.net/images/pdf/LDD3/ch13.pdf
- https://static.lwn.net/images/pdf/LDD3/ch14.pdf
- https://www.kernel.org/doc/html/v4.13/driver-api/usb/writing_usb_driver.html
- https://www.kernel.org/doc/html/v4.13/driver-api/usb/usb.html
- https://www.kernel.org/doc/html/v4.13/driver-api/usb/hotplug.html
- https://elixir.bootlin.com/linux/v2.6.33/source/include/linux/hid.h#L34
- https://elixir.bootlin.com/linux/latest/source/include/linux/printk.h
- https://elixir.bootlin.com/linux/latest/source/include/linux/init.h
- https://elixir.bootlin.com/linux/latest/source/include/linux/kernel.h

#### Misc device drivers
- https://linux-kernel-labs.github.io/refs/heads/master/labs/device_drivers.html#read-and-write
- https://www.kernel.org/doc/html/latest/driver-api/misc_devices.html#c.misc_register
- https://embetronicx.com/tutorials/linux/device-drivers/misc-device-driver/
- https://embetronicx.com/tutorials/linux/device-drivers/cdev-structure-and-file-operations-of-character-drivers/
- https://static.lwn.net/images/pdf/LDD3/ch03.pdf
- https://www.kernel.org/doc/htmldocs/kernel-hacking/routines-copy.html
- https://www.fsl.cs.sunysb.edu/kernel-api/re257.html
- https://elixir.bootlin.com/linux/latest/source/include/linux/uaccess.h

#### API
- https://www.kernel.org/doc/html/latest/locking/mutex-design.html#when-to-use-mutexes
- https://www.kernel.org/doc/html/v4.13/kernel-hacking/locking.html#mutex-api-reference
- https://cyberglory.wordpress.com/2011/08/21/jiffies-in-linux-kernel/
- https://www.kernel.org/doc/html/latest/core-api/kernel-api.html#c.snprintf
- https://elixir.bootlin.com/linux/latest/source/lib/vsprintf.c
- https://www.kernel.org/doc/htmldocs/kernel-api/API-snprintf.html
- https://www.kernel.org/doc/htmldocs/kernel-api/API-strncpy.html
- https://linux.die.net/man/3/strncpy

#### debugfs
- https://www.kernel.org/doc/html/latest/filesystems/debugfs.html#id2
- https://www.zachpfeffer.com/single-post/A-Quick-debugfs-Example

#### sysfs
- https://www.kernel.org/doc/html/latest/admin-guide/sysfs-rules.html
- https://www.kernel.org/doc/html/latest/filesystems/sysfs.html
- https://www.kernel.org/doc/html/latest/hwmon/sysfs-interface.html
- https://elixir.bootlin.com/linux/v4.14.5/source/Documentation/kobject.txt
- http://books.gigatux.nl/mirror/kerneldevelopment/0672327201/ch17lev1sec8.html

#### Linked lists
- https://www.fsl.cs.sunysb.edu/kernel-api/re252.html
- http://books.gigatux.nl/mirror/kerneldevelopment/0672327201/ch11lev1sec4.html
- https://elixir.bootlin.com/linux/latest/source/include/linux/list.h
- Link listed integrity, concurrency 
  - https://lore.kernel.org/lkml/20200324153643.15527-1-will@kernel.org/
- https://gitlab.inria.fr/lawall/liliput

#### Memory management
- https://linux-mm.org/
- https://www.tldp.org/LDP/tlk/mm/memory.html
- https://www.kernel.org/doc/html/latest/admin-guide/mm/concepts.html
- https://www.win.tue.nl/~aeb/linux/lk/lk-9.html
- https://en.wikibooks.org/wiki/The_Linux_Kernel/Memory
- https://www.youtube.com/watch?v=7aONIVSXiJ8
- https://static.lwn.net/images/pdf/LDD3/ch15.pdf
- https://learnlinuxconcepts.blogspot.com/2014/03/memory-layout-of-userspace-c-program.html
- https://developer.ibm.com/articles/l-kernel-memory-access/
- https://www.kernel.org/doc/html/v5.3/x86/exception-tables.html
- https://www.halolinux.us/kernel-reference/handling-the-tlb.html
- Sparse vs. flat memory 
  - https://lwn.net/Articles/789304/
  - https://lwn.net/Articles/134804/
  - https://forums.gentoo.org/viewtopic-p-6643251.html
- NUMA
  - https://www.kernel.org/doc/html/latest/vm/numa.html

#### TTY
- https://www.kernel.org/doc/html/latest/driver-api/serial/tty.html
- https://static.lwn.net/images/pdf/LDD3/ch18.pdf
- https://www.win.tue.nl/~aeb/linux/lk/lk-11.html

#### ASM/compiler stuff/etc
- https://refspecs.linuxbase.org/elf/gabi4+/ch4.reloc.html
- https://stffrdhrn.github.io/hardware/embedded/openrisc/2019/11/29/relocs.html
- https://docs.oracle.com/cd/E19641-01/802-1948/802-1948.pdf
- https://en.wikipedia.org/wiki/X86_instruction_listings
- https://refspecs.linuxbase.org/elf/x86_64-abi-0.98.pdf

#### Net
- https://en.wikipedia.org/wiki/Cyclic_redundancy_check
- https://en.wikipedia.org/wiki/Ethernet_frame
- http://lkml.iu.edu/hypermail/linux/kernel/9911.0/0202.html
- https://stackoverflow.com/questions/24530199/how-to-find-out-sk-buff-structure-size
- https://stackoverflow.com/questions/11169961/how-exactly-is-the-amount-of-space-allocated-to-a-to-be-transmitted-packet-skb-d
- https://www.kernel.org/doc/htmldocs/networking/API---netdev-alloc-skb.html
- https://en.wikipedia.org/wiki/Maximum_transmission_unit
- https://lkml.org/lkml/2020/3/5/926

#### USB
- https://usb.org.10-1-108-210.causewaynow.com/sites/default/files/CDC_EEM10.pdf
- Gadget
  - https://groups.google.com/g/syzkaller/c/wjQc3SSOTwU
  - https://www.kernel.org/doc/html/latest/usb/functionfs.html
  - https://www.collabora.com/news-and-blog/blog/2019/06/24/using-dummy-hcd/
  - https://blog.elastocloud.org/2016/06/linux-usb-gadget-application-testing.html
  - https://wiki.onakasuita.org/pukiwiki/?FunctionFS
  - https://elinux.org/images/6/66/Elc_2014_usb.pdf
  - https://s3.amazonaws.com/connect.linaro.org/sfo15/Presentations/09-23-Wednesday/SFO15-311-%ConfigFS%Gadgets-%An%Introduction.pdf
  - https://events.static.linuxfound.org/sites/events/files/slides/LinuxConNA-Make-your-own-USB-gadget-Andrzej.Pietrasiewicz.pdf
  - https://elinux.org/images/8/81/Useful_USB_Gadgets_on_Linux.pdf
  - https://wiki.tizen.org/USB/Linux_USB_Layers/Configfs_Composite_Gadget/General_configuration
  - https://en.wikipedia.org/wiki/Ethernet_over_USB#Protocols
  
#### Perf subsystem
- https://perf.wiki.kernel.org/index.php/Main_Page
- https://www.kernel.org/doc/html/v5.2/admin-guide/perf-security.html
- https://terenceli.github.io/%E6%8A%80%E6%9C%AF/2020/08/29/perf-arch
- Intel PTrace 
  - https://perf.wiki.kernel.org/index.php/Perf_tools_support_for_Intel%C2%AE_Processor_Trace#Introduction

#### Fuzzing/testing
- https://www.collabora.com/news-and-blog/blog/2020/04/17/using-syzkaller-to-detect-programming-bugs-in-linux/
- https://github.com/google/syzkaller/blob/master/docs/linux/setup.md
- https://github.com/google/syzkaller/blob/master/docs/linux/setup_ubuntu-host_qemu-vm_x86-64-kernel.md
- https://github.com/google/syzkaller/blob/master/docs/linux/kernel_configs.md
- https://github.com/dvyukov/syzkaller-repros
- https://groups.google.com/g/syzkaller/c/QbWWce5bPHc/m/zhSeTweOCAAJ
- https://groups.google.com/d/msg/syzkaller/RNp5Bg5pQZY/GwJ0KRqwBwAJ
- https://groups.google.com/d/msg/syzkaller/RQFLqAvdsEc/SHhXv50qCwAJ
- https://git.kernel.org/pub/scm/linux/kernel/git/shuah/linux-arts.git/
- https://github.com/google/syzkaller/blob/master/docs/reproducing_crashes.md
- https://github.com/google/syzkaller/blob/master/docs/executing_syzkaller_programs.md

#### Lockdep
- https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/tree/Documentation/locking/lockdep-design.rst?h=v5.9-rc5
- http://www.cs.albany.edu/~sdc/CSI500/Fal13/FindingLockdepReferences.html
- https://lwn.net/Articles/536363/
- https://lwn.net/Articles/321663/
- https://lwn.net/Articles/185666/

#### Misc
- https://koblents.com/Ches/Links/Month-Mar-2013/20-Using-Goto-/

#### Embedded linux
- Bootloaders
  - https://systemd.io/BOOT_LOADER_SPECIFICATION/
  - https://gitlab.denx.de/u-boot/u-boot/blob/master/doc/README.distro
- Device tree & device tree overlays
  - https://elinux.org/Device_Tree_Usage
  - https://elinux.org/Device_Tree_Reference
  - https://www.kernel.org/doc/html/latest/devicetree/usage-model.html
  - https://events.static.linuxfound.org/sites/events/files/slides/petazzoni-device-tree-dummies.pdf
  - https://en.wikipedia.org/wiki/Device_tree
  - https://www.kernel.org/doc/Documentation/devicetree/overlay-notes.txt
  - https://www.96boards.org/documentation/consumer/dragonboard/dragonboard410c/guides/dt-overlays.md.html
  - https://source.android.com/devices/architecture/dto
