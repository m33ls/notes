# fuzzing

notes on setting up a fuzzing environment

## instrumentation / sanitizers

AddressSanitizer

Compiler instrumentation for detecting errors in memory including; out-of-bounds access, use-afer-free, use-after-return, use-after-scope, double-free, invalid free, and memory leaks.

install
build llvm/clang with cmake
```
git clone https://github.com/llvm/llvm-project.git
cd llvm-project
mkdir build
cd build
cmake -DCMAKE_BUILD_TYPE=Release -DLLVM_ENABLE_PROJECTS="clang" -DLLVM_ENABLE_RUNTIMES="compiler-rt" ../llvm
make
```
installed to path:
```
.../llvm/build/bin
```
compile and link
```
llvm/build/bin/clang++ -O1 -g -fsanitize=address -fno-omit-frame-pointer <EXAMPLE>.cc
```
