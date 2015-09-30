# Learn command line

Please follow and complete the free online [Command Line Crash Course
tutorial](http://cli.learncodethehardway.org/book/). This is a great,
quick tutorial. Each "chapter" focuses on a command. Type the commands
you see in the _Do This_ section, and read the _You Learned This_
section. Move on to the next chapter. You should be able to go through
these in a couple of hours.


---

Make a cheat sheet for yourself: a list of at least **ten** commands and what they do, focused on things that are new, interesting, or otherwise worth remembering.

> > here are my 10 command(ments):

`hostname` -- name of the computer

`pushd`and `popd`--move around between directories

`touch something.txt` -- create an empty file called something.txt


---


---

What does `ls` do? What do `ls -a`, `ls -l`, and `ls -lh` do? What combinations of those flags are meaningful?

`ls` -- list directory contents

`ls -a` -- include files starting with .

`ls -l` -- use long listing with more information like access rights and dates

`ls -lh` -- print in human readable format like the size are appended with k or m

---


---

What does `xargs` do? Give an example of how to use it.

> > it will take as input the output of previous piped command and do useful stuff

for example:

`find . -name "*.txt"|xargs rm -rf`

will find any txt file in the current directly and remove them


I found helpful tutorial on `xargs` here: 
http://www.thegeekstuff.com/2013/12/xargs-examples/



---

