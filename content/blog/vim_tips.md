+++
Categories = ["Development", "GoLang"]
Description = ""
Tags = ["Development", "golang"]
date = "2015-05-13T10:01:28-04:00"
menu = "main"
title = "vim_tips"

+++


Find a space pattern and insert a newline,
useful for path variable expansion

    /\_s
    :s//\r&/g

