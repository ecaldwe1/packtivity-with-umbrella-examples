# Hello World Example
## A Packtivity example using Umbrella backend

This example uses [Umbrella](http://ccl.cse.nd.edu/software/manuals/umbrella.html) as the backend.

The specification file used in this example can be found [here](https://raw.githubusercontent.com/ecaldwe1/packtivity-with-umbrella-examples/master/fast.umbrella).

## About this example
This simple example will echo "Hello World" to the command line and then pipe that into the outputfile.

hello-world-example.yml:
```
process:
  process_type: 'string-interpolated-cmd'
  cmd: 'echo Hello {parone} | tee {outputfile}'
publisher:
  publisher_type: 'frompar-pub'
  outputmap:
    outputfile: outputfile
environment:
  environment_type: 'umbrella'
  image: 'centos6' 
  spec_url: 'https://raw.githubusercontent.com/ecaldwe1/packtivity-with-umbrella-examples/master/fast.umbrella'
```

You will notice that the packtivity spec environment refers to a spec called fast.umbrella. The fast.umbrella file is provided in the repository and the url to that file is already provided in the `.yml` file. Packtivity has been updated to allow a URL for the Umbrella specification file.

## Run the example

Now you are ready to run the packtivity. Run the following command to execute this packtivity.
```bash
packtivity-run hello-world-example.yml \
-p parone="World" \
-p outputfile="'{workdir}/outputfile'"
```

When the packtivity has finished running, you should see a new file in the directory you ran the command in. This is the outputfile specified in the command and specification. If you open this file, you will see that it has the same text as the given input file.


---
Simple Packtivity Examples Using Umbrella  
E. Caldwell - Center for Research Computing, University of Notre Dame  
last updated: 24 May 2017