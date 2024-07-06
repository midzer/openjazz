# Emscripten

## Build

```
emmake make
```

## Link

```
emcc -flto -O3 src/*.o src/*/*.o src/*/*/*.o src/*/*/*/*.o ext/*/*.o -o index.html -sUSE_SDL=2 -sASYNCIFY -sASYNCIFY_IGNORE_INDIRECT -sASYNCIFY_ONLY=@funcs.txt -sENVIRONMENT=web --preload-file data/ --preload-file openjazz.cfg --closure 1 -sEXPORTED_RUNTIME_METHODS=['allocate']
```
