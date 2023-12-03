# local_manifests

# Building KernelSU for Evolution X
1.) Sync the ROM source as stated in the Evolution X manifest:
    https://github.com/Evolution-X/manifest
    
2.) Setup the build environment and lunch your device e.g.:

    . build/envsetup.sh
    lunch evolution_lemonade/p-userdebug

3.) "cd" into the kernel directory and clone KernelSU as stated on
  https://kernelsu.org/guide/how-to-integrate-for-non-gki.html e.g.:
  
  ```
  cd kernel/oneplus/sm8350/
  curl -LSs "https://raw.githubusercontent.com/tiann/KernelSU/main/kernel/setup.sh" | bash -
  ```
  
4.) "cd" back to the root directory and run "m bootimage":

  ```
  cd ../../../
  m bootimage
  ```

5.) Flash the compiled kernel e.g:

  ```
  fastboot flash boot /home/imminent/android/evox/tiramisu/out/target/product/lemonadep/boot.img
  ```

6.) Reboot and enjoy KernelSU!

# Building the rom

For now local_manifests are required for the firmware & OnePlus camera, this is subject to change.
