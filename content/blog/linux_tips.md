+++
Categories = ["Development", "Linux"]
Description = ""
Tags = ["Development", "linux","tips","tutorial"]
date = "2015-05-11T20:53:46-04:00"
title = "linux_tips"

+++

For learning how to make bash shell scripts for linux. Recommend going through this [tutorial](http://www.freeos.com/guides/lsst/) list first 

### Filters
* **tail +20 < hotel.txt | head -n30 >hlist** takes lines 20 and is filtered  by head to 30 from hotel.txt and ouputs to hlist file.
* **sort < sname | uniq > u_sname** sorts the lines of sname file, and is filtered by uniq command.

### Relational Operators
* **10 -eq 10**: a is __equal__ to b
* **10 -ne 20**: a is __not equal__ to b
* **10 -gt 20**: a is not __greater__ than b
* **10 -lt 20**: a is __less__ than b
* **10 -ge 20**: a is not __greater or equal__ to b
* **10 -le 20**: a is __less or equal__ to b
* [ -e filepath ] Returns true if file exists.
* [ -x filepath ] Returns true if file exists and executable.
* [ -S filepath ] Returns true if file exists and its a socket file.
* [ expr1 -a expr2 ] Returns true if both the expression is true.
* [ expr1 -o expr2 ] Returns true if either of the expression1 or 2 is true.

### For Loops
    for ((  i = 0 ;  i <= 5;  i++  ))

    for (( expr1; expr2; expr3 ))
    do
       ### each expression will be evaluated ###  
    Done

    for (( i = 1; i <= 5; i++ ))      ### Outer for loop ###
    do
        for (( j = 1 ; j <= 5; j++ )) ### Inner for loop ###
        do
              echo -n "$i "
        done
      echo "" #### print the new line ###
    done


### Brace Expansion
    {a,b}$PATH  # is a$PATH b$PATH
    _{I,want,my,money,back} # is _I _want _my _money _back

    $ echo {5..12} # brace expansion
    5 6 7 8 9 10 11 12
    $ echo {5..k} # cannot mix types
    {5..k}
    $ echo {01..10} # zeropad, range is zeropadded as well
    01 02 03 04 05 06 07 08 09 10
    $ echo {{A..C},{a..c}} #also follows alphater 
    A B C a b c

### Redirection
| Standard File | Descriptor Number
| ---------|----
| stdin    | 0 
| stdout   | 1
| stderr   | 2

    $ rm bad_file_name111 > err.txt #prints the error on screen
    $ rm bad_file_name111 2>err.txt #redirects stderr output to the err.txt

    #edit ./demoscr
    echo "Error" 1>&2 #prints message as stderr
    cd nonexistent 2>&1 #redirects stderr of command to stdout
    1>filename # Redirect stdout to file "filename."
    1>>filename # Redirect and append stdout to file "filename."
    2>filename # Redirect stderr to file "filename."
    2>>filename # Redirect and append stderr to file "filename."
    &>filename # Redirect both stdout and stderr to file "filename."

    $ ./demoscr > er1   

### References
[tlp](http://www.tldp.org/LDP/abs/html/io-redirection.html)