# Input File Example 2
## a Packtivity example using Umbrella backend

This example uses [Umbrella](http://ccl.cse.nd.edu/software/manuals/umbrella.html) as the backend.

The specification file used in this example can be found at: https://raw.githubusercontent.com/ecaldwe1/packtivity-with-umbrella-examples/master/fast.umbrella
## How to run

```bash
rm -rf _packtivity
packtivity-run hello-world-example.yml \
  -p parone="World" \
  -p outputfile="'{workdir}/outputfile'"
```
