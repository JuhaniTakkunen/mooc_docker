Create Python3 environment using Docker. For this, a good startup point is: https://hub.docker.com/_/python

I also included custom requirements for this, lxml, requests and zeep. 


# run python file
```
# docker run -it -v "$PWD":/usr/src/app python-117 python hello.py
hello world
```

# run python from console
```
# docker run -it python-117 
Python 3.7.4 (default, Aug 14 2019, 12:09:51) 
[GCC 8.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> print("hei maailma")
hei maailma
```
# verify, that libraries work
```
>>> import requests
>>> print(requests.get("https://www.w3schools.com/xml/note.xml").text)
<?xml version="1.0" encoding="UTF-8"?>
<note>
  <to>Tove</to>
  <from>Jani</from>
  <heading>Reminder</heading>
  <body>Don't forget me this weekend!</body>
</note>
```
