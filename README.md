## Hello World for CMake on Linux

Example of how to build a C project that uses GTK4 with support for `clangd`.
Compilation database for `clangd` is generated by CMake with option `cmake -DCMAKE_EXPORT_COMPILE_COMMANDS=1`.

### Building
Requires `pkg-config`, `clangd`, `gtk4`, and `cmake`.

1. `mkdir build; cd build`
2. `cmake -DCMAKE_EXPORT_COMPILE_COMMANDS=1 ../`
3. `cp compile_commands.json ../`
4. `make`


## References
- http://www.voidcn.com/article/p-ollmkxzl-ya.html
- https://gnome.pages.gitlab.gnome.org/gtk/gtk/gtk-getting-started.html
- https://clangd.llvm.org/installation.html
