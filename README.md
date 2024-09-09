bochs compiled to Javascript using emscripten


bochs2.7, bochs2.7.pre1,bochs2.8,bochs2.8(1):

/home/user/emsdk/upstream/emscripten/emconfigure ./configure --target=x86_64-unknown-linux-gnu --host=x86_64-unknown-linux-gnu --with-rfb --enable-a20-pin --enable-x86-64 --enable-smp --enable-cpu-level=6 --enable-fpu --enable-vmx=2 --enable-svm --enable-3dnow --enable-avx --enable-cdrom --enable-xpm  --disable-debugger --disable-plugins

/home/user/emsdk/upstream/emscripten/emmake make -j6 -i

/home/user/emsdk/upstream/emscripten/em++ bochs.o -o bochs.js



bochs2.8-html:

/home/user/emsdk/upstream/emscripten/emconfigure ./configure --target=x86_64-unknown-linux-gnu --host=x86_64-unknown-linux-gnu --with-rfb --enable-a20-pin --enable-x86-64 --enable-smp --enable-cpu-level=6 --enable-fpu --enable-vmx=2 --enable-svm --enable-3dnow --enable-avx --enable-cdrom --enable-xpm  --disable-debugger --disable-plugins

/home/user/emsdk/upstream/emscripten/emmake make -j6 -i

/home/user/emsdk/upstream/emscripten/em++ bochs.o -o bochs.html



bochs2.8-SDL2: 

/home/user/emsdk/upstream/emscripten/emconfigure ./configure --target=x86_64-unknown-linux-gnu --host=x86_64-unknown-linux-gnu --with-sdl2 --enable-a20-pin --enable-x86-64 --enable-smp --enable-cpu-level=6 --enable-long-phy-address --enable-large-ramfile --enable-repeat-speedups --enable-fast-function-calls --enable-handlers-chaining --enable-trace-linking --enable-readline --enable-fpu --enable-vmx=2 --enable-svm --enable-3dnow --enable-memtype --enable-avx --enable-evex --enable-amx --enable-pci --enable-usb --enable-clgd54xx --enable-cdrom --enable-xpm  --disable-debugger --disable-plugins --without-x11
 
/home/user/emsdk/upstream/emscripten/emmake make -j6 -i
 
/home/user/emsdk/upstream/emscripten/em++ bochs.o -s USE_SDL=2 -O3 -o bochs.html --embed-file data@/
