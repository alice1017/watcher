# watcher - Watch the file moification

The **watcher** is Python module  about watching files modification using timestamp.

## How to Install

## How to Use

First, import this module.
Second, create `Watcher` class's instance.
Third, append file or files to instance.
Fourth, using Python with sentence, You can write anything under with sentence.

```python
#!/usr/bin/python

import os
from watcher import Watcher

files = os.listdir(".") # >>> ['sample.txt', 'sample.py']

# create Watcher instnce
watcher = Watcher()

# append file to watcher instance
watcher.add_file("sample.txt",)

# or 

# append files to watcher instance
watcher.add_files(os.listdir("."),)

# start watch using with sentence
# you can write anything under with sentence.
# If watcher catch file modification, watcher run anything you written
for mdf in watcher.watch():
    
    print mdf.name.center(20, "=")
    print "Catch the Modification!!"
    print "New timestamp: %s" % mdf.timestamp
    print "="*20

```

