Docker container for running [Folding@Home](http://folding.stanford.edu/)

### Usage
```bash
docker run --rm -d --name fah -p7396:7396 benkorichard/folding-at-home:latest
```

By default it'll start the client as anonymous, with disabled gpu and full power.

You can edit these options by passing them as command:

```bash
docker run --rm -d --name fah -p7396:7396 benkorichard/folding-at-home:latest \
--user=<username> --team=<team_id> --gpu=false --smp=true --power=full
```

An example compose file:

```yml
---
version: '3.7'

services:
  folding-at-home:
    image: benkorichard/folding-at-home:latest
    ports:
      - 7396:7396
    command: --user=<username> --team=<team> --gpu=false --smp=true --power=full
```


The web console is available on port `7396`.
