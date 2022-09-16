# prime-run-linux
So that I don't forget

1. Make sure the NVIDIA drivers are installed and reboot if you just installed them.
2. Open a terminal and type: nano prime-run
3. Copy and paste this script into nano, then save and quit nano:
#!/bin/bash
__NV_PRIME_RENDER_OFFLOAD=1 __VK_LAYER_NV_optimus=NVIDIA_only __GLX_VENDOR_LIBRARY_NAME=nvidia "$@"
4. In terminal type:
$ sudo mv prime-run /bin
$ cd /bin
$ sudo chmod 755 prime-run
5. Test it by typing prime-run glxinfo | grep "OpenGL renderer"
6. Now type prime-run any-app (i.e. prime-run firefox) and the application will run using the GPU.
7. To check if the application is being run on the GPU, type nvidia-smi in the terminal and it will show a list of applications using the GPU.

https://www.youtube.com/watch?v=aPi8NfDyDMU
