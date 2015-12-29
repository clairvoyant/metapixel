OBJS = readimage.o writeimage.o rwpng.o rwjpeg.o rwgif.o

CCOPTS = -I/usr/local/include

FORMATDEFS = -DRWIMG_PNG -DRWIMG_JPEG -DRWIMG_GIF

all : librwimg.a

librwimg.a : $(OBJS)
	ar rcu librwimg.a $(OBJS)

%.o : %.c
	$(CC) $(CCOPTS) $(FORMATDEFS) -g -c $<

clean :
	rm -f *~ $(OBJS) librwimg.a
