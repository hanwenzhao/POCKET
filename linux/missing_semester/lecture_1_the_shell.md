# MIT Missing Semester

# Lecture 1: The Shell

## echo
echo Hello "Hello" 'Hello' 'Hello\ World'

## environment Variable
echo $PATH\
(Linux will search through path to for any program you run)

## which
which echo\
(Linux will tell you the path to the program)

## pwd
(print working directory)

./ (current directory)\
../ (parent directory)\

## help
ls --help or ls -h

## permissions
drwxrwxrwx
d---------: directory or not\
-rwx------: permission of the owner\
----rwx---: permission for the group\
-------rwx: permission for everyone else\

## mv
mv [source] [destination]
cp [source] [destination]

## rm
remove in default is not recursive, add flag -r

## man
manual page

## ctrl + L
clean the current bash

## streams
input stream: keyboards
output stream: print

we can rewire the streams:\
< program > file\
<: rewire the input of the program\
\>: rewire the output of the program\
\>\>: append instead of write

ex:\
echo hello > hello.txt

## cat
cat hello.txt\
print the content of the file\

cat < hello.txt > hello2.txt\
cat will open hello.txt and copy the content to hello2.txt

## pipe '|'
program 1 | program 2\
take the output of program 1 and use it as the input for program 2

## tail
tail -n 10\
print the last 10 lines of the output

## root user (super user)
$ symbol - non-root user
\# symbol - root user
### Entering the kernel file system
cd /sys

$echo 500 > /sys/intel_backlight/brightness will not work, the shell is running under non-root user

echo 500 | sudo tee brightness will work, because tee is running as sudo 

echo 1 | sudo tee /sys/leds/scrolllock (control the led on the scoll lock key)


## Cool Examples
curl --head --silent google.com | grep -i(ignore-case) content length | cut --delimiter=' ' -f2


# Lecture 2













