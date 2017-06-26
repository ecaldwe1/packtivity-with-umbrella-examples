## Examples of running Packtivity using Umbrella environment

This repository contains examples to illustrate packtivities running using Umbrella.

Please note that the packtivity and yadage-schemas used in this repository have been modified to accomodate Umbrella as 
an environment. The modified code can be found in these repositories: [Packtivity](https://github.com/ecaldwe1/packtivity) [Yadage-Schemas](https://github.com/ecaldwe1/yadage-schemas). 

The changes required to add Umbrella are found in:
 - `packtivity/packtivity/handlers/environment_handlers.py`
 - `yadage-schemas/yadage-schemas/packtivity/environment/umbrella.json` (new file)
 - `yadage-schemas/yadage-schemas/packtivity/packtivity-schema.json`

These examples **will not run** if you are currently using these versions of [Packtivity](https://github.com/diana-hep/packtivity) or [Yadage-Schemas](https://github.com/diana-hep/yadage-schemas).

### [Wiki](https://github.com/ecaldwe1/packtivity-with-umbrella-examples/wiki) Pages:
 - [Setting up your Environment](https://github.com/ecaldwe1/packtivity-with-umbrella-examples/wiki/Setting-Up-Environment)
 - [Creating Virtual Environments](https://github.com/ecaldwe1/packtivity-with-umbrella-examples/wiki/Creating-Virtual-Environments)
 - [Types of Umbrella Specification in the Packtivity Spec](https://github.com/ecaldwe1/packtivity-with-umbrella-examples/wiki/Type-of-Umbrella-Specification)

### Examples:
 - [**Hello World Example**](https://github.com/ecaldwe1/packtivity-with-umbrella-examples/tree/master/hello-world-example)
 
   Very basic example that runs a command and creates an output file with the result of the command. The Packtivity specification in this example uses a URL to the Umbrella specification file.
   
   See the instructions within the _hello-world-example_ directory for details on how to run this example.
   
 - [**Input File Example**](https://github.com/ecaldwe1/packtivity-with-umbrella-examples/tree/master/input-file-example)
   
   Example illustrates that using Packtivity with Umbrella in a workflow context is viable. 
   This example takes an input file as a parameter and saves the contents of the input file into an output file. The Packtivity specification in this example uses a URL to the Umbrella specification file.
   
   See the instructions within the _input-file-example_ directory for details on how to run this example.
   
 - [**Input File Example 2**](https://github.com/ecaldwe1/packtivity-with-umbrella-examples/tree/master/input-file-example2)
   
   This example takes an input file as a parameter and saves the contents of the input file into an output file, however the difference between this example and the Input File Example above, is that the input file is read from an inputs directory and the output file is written to an outdir, similar to the example on the [Packtivity GitHub page](https://github.com/diana-hep/packtivity). The Packtivity specification in this example uses a URL to the Umbrella specification file. 
   
   See the instructions within the _input-file-example-2_ directory for details on how to run this example.
   
 - [**Hello World Example with Reference to the Umbrella Specification**](https://github.com/ecaldwe1/packtivity-with-umbrella-examples/tree/master/hello-world-example-full-spec-ref)
 
   Runs a command and creates an output file with the result of the command, just as in the [Hello World Example](https://github.com/ecaldwe1/packtivity-with-umbrella-examples/tree/master/hello-world-example), however the Packtivity specification in this example uses a reference to the Umbrella specification file. Details on the different ways to include the Umbrella specification can be found on the wiki [here](https://github.com/ecaldwe1/packtivity-with-umbrella-examples/wiki/Type-of-Umbrella-Specification).
   
   See the instructions within the _hello-world-example-full-spec-ref_ directory for details on how to run this example.
