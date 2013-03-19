Terminal Tips
=============
Everyday terminal tips to make a developers life easier.


**Tip**: A sample tip

**Description**: A sample description

Follow the template above and keep appending. Make sure you add your name/link your github profile at the end:-)

---

**Tip**: `!$`

**Description**: Execute the last command which was just executed.

---

**Tip**: `> file.txt`

**Description**: Truncates a file it exists or creates an empty file.


---

**Tip**: `echo "hello, world" | at  midnight`

**Description**: Runs the command specified at midnight. It can be very verbose like `at 6pm tomorrow` or `at now +2minute` or `2am next year`. use `man at` to know more about the at command.

---

**Tip**: `rm -f !(file.txt)`

**Description**: Remove all files execpt `file.txt`.

---

**Tip**: `ls -1 | wc -l`

**Description**: Count all files in a directory. 

---

**Tip**: `hash`

**Description**: Prints the number of times a command is executed in the current terminal session.

---

**Tip**: `tar --transform 's, ^, PREFIX,' -c -f TARGET.tar <FILES>`

**Description**: Prepend "PREFIX" to each file while archiving. Useful when you
want to create a common top level directory hierarchy for all the files being
archived. For example:

tar --transform "s, ^, $PKGNAME-$VERSION/, S" -czpf "$PKGNAME-$VERSION.tar.gz" -C "$BASEDIR/$BASENAME" \
Symfony SampleConfs Scripts activemq

S - does not apply transformation to symbolic link targets

----

**Tip**: `tar -czf TARGET.tar.gz <FILES> --checkpoint --checkpoint-action='ttyout=archiving... %u  \r'`

**Description**: provides a nice progress status of archiving process when you
dont want to use -v option to keep a track of what is happening. checkpoint
option can be modified to provide a % progress status bar

----

**Tip**: `tar -czvf TARGET.tar.gz -X exclude.txt <FILES>`

**Description**: Exclude a list of unwanted files. Usually when creating a
package you would not want a certain dirs or file. All those unrequired files
can be put into a file and specified with tar so that those files will be
excluded while archiving.
Example:

tar --transform "s, ^, $PKGNAME-$VERSION/, S" -czpf "$PKGNAME-$VERSION.tar.gz" -X exclude.txt \
-C "$BASEDIR/$BASENAME" Symfony SampleConfs Scripts activemq --checkpoint \ 
--checkpoint-action='ttyout=archiving... %u  \r'

---



Contributers
============

* [Sandeep Raju](http://github.com/sandeepraju/)
* [Nitheesh K L](http://github.com/nitheeshkl/)
