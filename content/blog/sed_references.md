+++
Categories = ["Development", "Linux"]
Description = ""
Tags = ["Development", "Sed", "Linux"]
date = "2015-05-12T10:06:44-04:00"
title = "sed_references"

+++

Sed stream editing command and awk command deserves their own reference post.
This is mainly a reference to the [grymoire][] article. 

    sed 's/\/usr\/local\/bin/\/common\/bin/' <old >new #Ugly
    sed 's_/usr/local/bin_/common/bin_' <old >new #Pretty underscore delimiters
    sed 's:/usr/local/bin:/common/bin:' <old >new #Pretty colon delimiters
    sed 's/[a-zA-Z]* /REPLACED /2' <old >new # only the second pattern occurrence
    sed 's/[a-zA-Z]* /REPLACED /2g' <old >new # replace all starting at second pattern



[grymoire]: http://www.grymoire.com/Unix/Sed.html#uh-0

