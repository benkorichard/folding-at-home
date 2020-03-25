Docker container for running [Folding@Home](http://folding.stanford.edu/)

### Usage
```bash
docker run --rm -it -p7396:7396 benkorichard/folding-at-home:latest \
    --user=John_Tims --team=11675 --gpu=false --smp=true --power=full
```

The web console is available on port `7396`.
