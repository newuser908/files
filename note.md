Echo-V2.8 (26404)

Diffs to official Magisk

    [App] Fix BT when SUList is enforced.
    [App] Added a new feature to install Magisk into /system partition for emulators that do not have a boot image.
    [Zygisk] Changed the method of loading Zygisk to ptrace init implementation (required Android 8+). The implementation comes from ZygiskNext. This method does not need to change any property and is more compatible with some emulators that ignore ro.dalvik.vm.native.bridge property.
    [Zygisk] Restore access to global tmpdir for zygote
    [General] Enhanced the support for mounting in pre-init for modules. This enables modules to modify the system before the init process starts, which can be useful for some advanced use cases.
    [General] Fix Magisk crashes which were caused by zygisk enabled on some devices.
    [General] Fix bootloop on some devices.
    [General] Implemented a new feature to support deleting file by using indicated whiteout character device, similar to overlayfs. This allows modules to delete files from the original system without actually modifying it.
    [General] Restored support for devices with no selinux support, which was removed by the official Magisk. This allows users to use Magisk on devices that do not have selinux enabled in kernel.


Diffs to v26.4

    [Zygisk] Introduce new code injection mechanism
    [Zygisk] Support new signature introduced in U QPR2
    [SEPolicy] Update libsepol to properly set some policy config bits
    [MagiskBoot] Support compressing init so Magisk is installable on devices with small boot partitions

