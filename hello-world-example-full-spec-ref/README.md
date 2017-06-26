# Hello World Example with Reference to the Umbrella Specification
## A Packtivity example using Umbrella backend

This example uses [Umbrella](http://ccl.cse.nd.edu/software/manuals/umbrella.html) as the backend.

The specification file used in this example can be found [here](https://raw.githubusercontent.com/ecaldwe1/packtivity-with-umbrella-examples/master/fast.umbrella).

## About this example
This example will echo "Hello World" to the command line and then pipe that into the outputfile.

The difference between this Hello World example and the original [Hello World Example](https://github.com/ecaldwe1/packtivity-with-umbrella-examples/tree/master/hello-world-example) is that the entire Umbrella 
specification is referenced in the Packtivity specification.

hello-world-example-full-spec-ref.yml:
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
  spec: {$ref: 'fast.umbrella.yaml'}
```

You will notice that the packtivity spec environment refers to a `spec` which is a reference to the Umbrella 
specification file. Umbrella expects the specification file to be a JSON file, but the Packtivity specification is a 
YAML file. To include the reference in the Packtivity specification, the JSON Umbrella specification will need to be 
converted to YAML. Scripts to accomplish this can be found [here](https://github.com/ecaldwe1/file-type-converters). 
(A PyPI package is in the works. This documentation will be updated when the PyPI package is available.) Packtivity
has been updated to convert a reference to a YAML Umbrella specification back to JSON before running the Umbrella 
command.

## Run the example

Running the packtivity is the same as before. Run the following command to execute this packtivity.
```bash
packtivity-run hello-world-example.yml \
-p parone="World" \
-p outputfile="'{workdir}/outputfile'"
```

When the packtivity has finished running, you should see a new file in the directory you ran the command in. This is the outputfile specified in the command and specification. If you open this file, you will see that it has the same text as the given input file.


---
Simple Packtivity Examples Using Umbrella  
E. Caldwell - Center for Research Computing, University of Notre Dame  
last updated: 26 June 2017