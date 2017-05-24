# Input File Example 2
## a Packtivity example using Umbrella backend

This example uses [Umbrella](http://ccl.cse.nd.edu/software/manuals/umbrella.html) as the backend.

The specification file used in this example can be found [here](https://raw.githubusercontent.com/ecaldwe1/packtivity-with-umbrella-examples/master/fast.umbrella).

## About this example
The example is similar to the other input example, however we have moved the 'myinputfile.txt' into the 'Inputs' directory and will write the output of the command to the 'outdir' directory.

This simple example will take the contents of an input file and save them in an output file. We use the same packtivity specification as in the other input file example, however we will run the command a little differently. Additionally, our file structure is different because we have our input file located inside a directory called **/inputs**

input-example.yml:
```
process:
  process_type: 'string-interpolated-cmd'
  cmd: 'cat {inputfile} > {outputfile}'
publisher:
  publisher_type: 'frompar-pub'
  outputmap:
    outputfile: outputfile
environment:
  environment_type: 'umbrella'
  image: 'centos6'
  spec_url: '/home/beth/Desktop/DASPOS/fast.umbrella'
```
You will notice that the packtivity spec environment refers to a spec called fast.umbrella. The fast.umbrella file is provided in the repository and the url to that file is already provided in the `.yml` file. Packtivity has been updated to allow a URL for the Umbrella specification file.

## Run the example
Now you are ready to run the packtivity. Run the following command to execute this packtivity.
```bash
packtivity-run input-example.yml \
-p inputfile="$PWD/inputs/myinputfile.txt" \ 
-p outputfile="'{workdir}/outputfile'" \
--read inputs \
--write outdir
```
When the packtivity has finished running, you should see a new directory in the directory you ran the command in. This is the outdir and will contain the _packtivity and outputfile specified in the command and specification. If you open this output file, you will see that it has the same text as the given input file.


---
Simple Packtivity Examples Using Umbrella  
E. Caldwell - Center for Research Computing, University of Notre Dame  
last updated: 24 May 2017
