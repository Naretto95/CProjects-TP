CP = cp
srcdir=./src/
bindir=./bin/
docdir=./doc/
savedir=./save/
CC= gcc -Wall
RM = rm -rf
SRC=$(wildcard $(srcdir)*.c)
HEAD=$(wildcard $(srcdir)*.h)
OBJ=$(subst $(srcdir),$(bindir),$(SRC:.c=.o))
PROG=tp6

$(PROG) : $(OBJ)
	$(CC) $^ -o $@

$(bindir)%.o: $(srcdir)%.c
	$(CC) -c $^ -o $@

.PHONY : clean save

clean:
	rm -f $(bindir)*.o core

save : 
	$(CP) $(srcdir)* $(savedir)

restore :
	$(CP) $(savedir)* $(srcdir)
