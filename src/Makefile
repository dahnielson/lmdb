CC := cl
CFLAGS := -nologo /O2 /MT /TC /c

.PHONY: all clean

all: ..\mdb.lib

clean:
	del mdb.obj midl.obj ..\mdb.lib

..\mdb.lib: mdb.obj midl.obj
	lib -nologo $^ -out:..\mdb.lib

mdb.obj: mdb.c lmdb.h midl.h
	$(CC) $(CFLAGS) mdb.c

midl.obj: midl.c midl.h
	$(CC) $(CFLAGS) midl.c
