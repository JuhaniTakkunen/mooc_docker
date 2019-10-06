NOTE: I also changed Dockerfiles to download data from git. Otherwise I would always have to copy the data and it's easier to test this this way. 
NOTE2: I also had to fix some paths (I think I fixed them incorrectly earlier) to fully allow node container to work without serve
```
back                                       latest              499f8fb18f2d        23 minutes ago      140MB
front                                      latest              40418b9ad4e5        12 minutes ago      236MB

test-back                                  latest              56b5ed426e72        6 hours ago         325MB
test-front                                 latest              153ae5e6c7b2        6 hours ago         588MB
```
