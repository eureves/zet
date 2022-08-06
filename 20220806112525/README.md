# First zettelkasten made with my little bash script

I've diced to not waste my time creating folders and md's in them, so I wrote a bash script to do it for me.
All it does is just creates folder with isosec name and a `README.md` file in it.

This is what it looks like. 

```bash
#!/bin/bash

d=`date +%Y%m%d%H%M%S`

mkdir ~/zet/$d
touch ~/zet/$d/README.md
vi ~/zet/$d/README.md
```

Much far from what rwxrob has made.

#bash #zettelkasten
