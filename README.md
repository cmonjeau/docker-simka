### Simka v.1.3.2 description ###

Simka is a comparative metagenomics method dedicated to NGS datasets. 

It computes a large collection of distances classically used in ecology to compare communities by approximating species counts by k-mer counts.

https://github.com/GATB/simka/tree/v1.3.2

### Print Simka using docker###

```
docker run -it --rm cmonjeau/simka /opt/simka/build/bin/simka
docker run -it --rm cmonjeau/simka /opt/simka/build/bin/simka -in /opt/simka/example/simka_input.txt -out results -out-tmp temp_output
docker run -it --rm cmonjeau/simka python /opt/simka/scripts/create_heatmaps.py results
```

### Run simka using Godocker (http://www.genouest.org/godocker/)

Create a new job with these parameters:

"Container image" : cmonjeau/simka

"Command" : 

```

#!/bin/bash

# command line example (adapt with your data)
/opt/simka/build/bin/simka -in $GODOCKER_HOME/simka_input.txt -out $GODOCKER_HOME/results -out-tmp temp_output

```

"Mount volumes" : home(rw)


