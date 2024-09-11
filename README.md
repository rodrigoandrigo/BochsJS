bochs compiled to Javascript using emscripten


bochs2.8-SDL2-cmdmode: 

/home/user/emsdk/upstream/emscripten/emconfigure ./configure --target=x86_64-unknown-linux-gnu --host=x86_64-unknown-linux-gnu --with-sdl2 --enable-a20-pin --enable-x86-64 --enable-smp --enable-cpu-level=6 --enable-long-phy-address --enable-large-ramfile --enable-repeat-speedups --enable-fast-function-calls --enable-handlers-chaining --enable-trace-linking --enable-readline --enable-fpu --enable-vmx=2 --enable-svm --enable-3dnow --enable-memtype --enable-avx --enable-evex --enable-amx --enable-pci --enable-usb --enable-clgd54xx --enable-cdrom --enable-xpm  --disable-debugger --disable-plugins --without-x11
 
/home/user/emsdk/upstream/emscripten/emmake make -j6 -i
 
/home/user/emsdk/upstream/emscripten/em++ bochs.o -s USE_SDL=2 -s FULL_ES2=1 -s ALLOW_MEMORY_GROWTH=1 -O0 -s EXPORTED_FUNCTIONS="['_main']" -o bochs.html --embed-file data@/

bochs2.8-SDL2-fullscreen: 

/home/user/emsdk/upstream/emscripten/emconfigure ./configure --target=x86_64-unknown-linux-gnu --host=x86_64-unknown-linux-gnu --with-sdl2 --enable-a20-pin --enable-x86-64 --enable-smp --enable-cpu-level=6 --enable-long-phy-address --enable-large-ramfile --enable-repeat-speedups --enable-fast-function-calls --enable-handlers-chaining --enable-trace-linking --enable-readline --enable-fpu --enable-vmx=2 --enable-svm --enable-3dnow --enable-memtype --enable-avx --enable-evex --enable-amx --enable-pci --enable-usb --enable-clgd54xx --enable-cdrom --enable-xpm  --disable-debugger --disable-plugins --without-x11
 
/home/user/emsdk/upstream/emscripten/emmake make -j6 -i
 
/home/user/emsdk/upstream/emscripten/em++ bochs.o -s USE_SDL=2 -s FULL_ES2=1 -s ALLOW_MEMORY_GROWTH=1 -O0 -s EXPORTED_FUNCTIONS="['_main']" -o bochs.html --embed-file data@/


