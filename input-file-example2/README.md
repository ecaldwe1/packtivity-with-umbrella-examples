# Input File Example 2
## a Packtivity example using Umbrella backend

This example uses [Umbrella](http://ccl.cse.nd.edu/software/manuals/umbrella.html) as the backend.
The example is similar to the other input example, however we have moved the 'myinputfile.txt' into the 'Inputs' directory and will write the output of the command to the 'outdir' directory.

## How to run

```bash
packtivity-run input-example.yml \
-p inputfile="$PWD/inputs/myinputfile.txt" \ 
-p outputfile="'{workdir}/outputfile'" \
--read inputs \
--write outdir
```