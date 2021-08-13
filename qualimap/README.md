# Build the dockerfile
docker build . -t qualimap

# Run qualimap
docker run --rm -ti qualimap qualimap --help

# If you want to push any update
docker tag qualimap gvcn/qualimap
docker push gvcn/qualimap:tag

# Run from dockerhub
docker pull gvcn/qualimap
docker run --rm -ti gvcn/qualimap qualimap --help
docker run --rm -v /your/data/dir:/data gvcn/qualimap qualimap <tools> <options>