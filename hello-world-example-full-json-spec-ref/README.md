# Hello World Example with Reference to the Umbrella Specification
## A Packtivity example using Umbrella backend

This example uses [Umbrella](http://ccl.cse.nd.edu/software/manuals/umbrella.html) as the backend.

The specification file used in this example can not contain any tabs. Use spaces instead!

## About this example
This example will echo "Hello World" to the command line and then pipe that into the outputfile.

The difference between this Hello World example and the original [Hello World Example](https://github.com/ecaldwe1/packtivity-with-umbrella-examples/tree/master/hello-world-example) is that the entire Umbrella 
specification is referenced in the Packtivity specification.

hello-world-example-full-json-spec-ref.yml:
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
  spec: {$ref: 'no-tabs-fast.umbrella'}
```

You will notice that the packtivity spec environment refers to a `spec` which is a reference to the Umbrella 
specification file. Umbrella expects the specification file to be a JSON file. To include the reference to the JSON specification in the Packtivity specification, the JSON Umbrella specification will need to have all tabs removed. Tabs have a special meaning in YAML and the parser is confused. Please make sure your Umbrella specification file uses spaces instead of tabs before including it as a reference in the Packtivity specification.

## Run the example

Running the packtivity is the same as before. Run the following command to execute this packtivity.
```bash
packtivity-run hello-world-example-full-json-spec-ref.yml \
-p parone="World" \
-p outputfile="'{workdir}/outputfile'"
```

When the packtivity has finished running, you should see a new file in the directory you ran the command in. This is the outputfile specified in the command and specification. If you open this file, you will see that it has the same text as the given input file.


---
Simple Packtivity Examples Using Umbrella  
E. Caldwell - Center for Research Computing, University of Notre Dame  
last updated: 30 June 2017