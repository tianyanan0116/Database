CC=gcc
AFLAGS=-Wall -g
LDFLAGS= -lmysqlclient
OBJS= add.cgi del.cgi mod.cgi sel.cgi deleteforever.cgi stulogin.cgi teacherlogin.cgi selcourse.cgi addscore.cgi selscore.cgi selectcourse.cgi selselectcourse.cgi selteacher-course.cgi

all:$(OBJS)

$(OBJS):%.cgi:%.c
	$(CC) $(AFLAGS) $< cgic.c -o $@ $(LDFLAGS)

.PHONY:clean
clean:
	rm ./*.cgi
install:
		cp *.cgi /usr/lib/cgi-bin/sx
		cp head.html footer.html stulogin.html teacherlogin.html /usr/lib/cgi-bin/sx/
