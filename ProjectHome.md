Egypt (http://www.gson.org/egypt/egypt.html) is a Perl script to generate call graphs with graphviz (dot, neato...) but when parses a C++ call it generates an ugly output.

**Regypt** renames all the functions to simple numbers.

Example of use:
```
$ g++ -dr someFile.cpp -o a.bin
$ egypt *expand > outputFromEgypt.txt
$ python regypt.py outputFromEgypt.txt > inputForNeato.gv
$ neato -T png -o output.png inputForNeato.gv
```

This will generate a call graph for someFile.cpp where each function is a number.