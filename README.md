# decompiler-helper-ideas
Just for logging some ideas for a decompiler addon

1. If-else-else-else -> switch + case
2. Transforming `*ptr` -> `ptr[0]` if there are `ptr[n]` which (n != 0).
3. C pseudo code to python converter (AST is given, so emulator / language converter is possible?) - will be useful with symbolic engines like z3py.
4. Additional calling convention supporter (I think that some microcode hack can do this. Ex: Go returns value to stack variable, Rust uses xmm registers before assigning actual rdi/rsi/... to copy some structures - some heuristics can help it, ...)
5. (solved) Decompiler can just emit DWARF symbols I guess? I mean, IDA2GDB. I doubt it as helpful for now. --> https://github.com/ALSchwalm/dwarfexport
6. arbitrary assembler -> microcode / retdec IR(I remember it has LLVM -> their IR pass) converter -> since microcode is opened, I guess decompilers for many architectures can be supported. Maybe there can be some hacks for some architecture, but decompiler itself is invaluable since viewing C and understanding heuristics is better than viewing assembly alone.
7. retdec variable name renamer? since retdec is open sourced, can we get some AST for it and save/sync some info with IDA(ex. stack variables, register assignment, ...)
8. drawing xref map to get some path information
9. C code patcher! (binary code patching itself does require lot of heuristics / architecture dependent things, it can be separated as another subject) would be great if I can write some code in C and apply to it. Will it require some deep-learning for generating correct code?! (nope)
10. It's not a plugin idea, but docs for decompiler internals will be great... Like, angr/S2E docs are improving. They're great.
