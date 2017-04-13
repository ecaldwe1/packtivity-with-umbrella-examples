# Tarball backend example

This is an example of using tarball backend. Docker image is imported from filesystem snapshot (tar.gz) -
from local or external file.

# How to run

```bash
rm -rf _packtivity
packtivity-run tarball.yml -p outputfile=/tmp/out.txt
```