# Hello World - an Umbrella example

This example uses [Umbrella](http://ccl.cse.nd.edu/software/manuals/umbrella.html) as the backend.

# How to run

```bash
rm -rf _packtivity
packtivity-run hello-world-example.yml \
  -p parone="World" \
  -p outputfile="'{workdir}/outputfile'"
```