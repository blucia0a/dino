# DINO Passes for LLVM

Our LLVM passes are built "out of source," meaning you can install LLVM
separately and simply load our passes as modules with LLVM's opt tool.

First build LLVM and install it in /path/to/llvm.

Then, in this directory, run

    $ cmake -DDINO_LLVM_DIR=/path/to/llvm
    $ make

Then you can load the passes via opt.  (TODO: document this)
