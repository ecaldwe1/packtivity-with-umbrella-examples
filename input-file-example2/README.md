# Input File - an Umbrella example

This example uses [Umbrella](http://ccl.cse.nd.edu/software/manuals/umbrella.html) as the backend.

# How to run

```bash
packtivity-run input-example.yml \
-p inputfile="$PWD/inputs/myinputfile.txt" \ 
-p outputfile="'{workdir}/outputfile'" \
--read inputs \
--write outdir
```