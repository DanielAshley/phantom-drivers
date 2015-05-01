# Getting it to work with Mac OS X #

Since libraw1394 is not available for MAC OS X, the native? MAC OS X libraries are used.

In order to compile the library against these libraries, add FW\_METHOD=macosx flag to the make command. To run the tests use:
```
 make FW_METHOD=macosx test
```

If you alway want to compile for Mac OS X add this flag to the Makefile itself.

**Note**: Mac OS X currently does _not_ support isochronous transfers yet.