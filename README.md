# decompiler-helper-ideas
Just for logging some ideas for a decompiler addon

1. If-else-else-else -> switch + case
2. Transforming `*ptr` -> `ptr[0]` if there are `ptr[n]` which (n != 0).
3. C++ to python converter (AST is given, so emulator / language converter is possible?)
4. Additional calling convention supporter (I think that some microcode hack can do this. Ex: Go returns value to stack variable, Rust uses xmm registers before assigning actual rdi/rsi/... to copy some structures - some heuristics can help it, ...)
