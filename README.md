# cliper
## Overview
Cliper save your text. The file is saved at ~/.cliper.txt.

## Demo

## Description
Save your keywords that you can't remember but you use sometime. The goal of this tool is useful for the person who don't want to open other tool.

Save keyword.  
``` bash
$ cliper -c 'ssh demo@192.168.0.1' 
Copied!!

$ cliper -c 'export KUBECONFIG="$(kind get kubeconfig-path --name="kind")"'
Copied!!
```

show specific keyword.
``` bash
$ cliper -p 1
ssh demo@192.168.0.1
```

Show all keyword.
``` bash
$ cliper
1: ssh demo@192.168.0.1
2: export KUBECONFIG="$(kind get kubeconfig-path --name="kind")"
```

Delete unuse keyword.
``` bash
$ cliper -d 1
Deleted!!

$ cliper
1: export KUBECONFIG="$(kind get kubeconfig-path --name="kind")"
```

If you want to delete whole of keywords. This file will make automatically when you use cliper.
``` bash
rm ~/.cliper.txt
```

There are three options.

``` bash  
optional arguments:
  -h, --help            show this help message and exit
  -c COPY, --copy COPY  Copy the keyward from stdin.
  -p PASTE, --paste PASTE
                        Print the specific keyward.
  -d DELETE, --delete DELETE
                        Delete the copied keyword.
```

# Install
Cliper is command. So, download and move the cliper file to under your PATH directory.

e.g.  
``` bash
mv cliper /usr/local/bin/cliper
```

# Authors
sourjp

# License
This project is licensed under the MIT License - see the LICENSE file for details
