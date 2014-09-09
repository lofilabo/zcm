zcm
===

Basic Cmake set, 2014 09 09

This file is a very minimal base for a project based around Cmake / make / gcc.
Add any number of .c and .h files, making sure to update the following:

Application references:
In this example, grep for rhello and replace it with your project name.


SET(HDRS 
  hello.h
  <----your new header files go here, one per line
)
and
SET(SRCS
  hello.c
  <----your new source files go here, one per line  
)

Note that the section about Doxygen is commented out, but left in for reference.
The usual order of compilation and deplyment is:

cmake .       #  execute cmake and generate the makefiles  
make          #  run the makefiles
make install  #  install the application, in this example to /bin
rhello        #  test run the installed application

