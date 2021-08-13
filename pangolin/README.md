# Build dockerfile
```
docker build . -t pangolin
```

# Run Pangolin
```
docker run --rm -ti pangolin pangolin --help
```

# Using dockerhub
```
# create tags
docker tag pangolin gvcn/pangolin
docker tag pangolin gvcn/pangolin:v3.1.11
# push to dockerhub
docker push gvcn/pangolin
docker push gvcn/pangolin:v3.1.11
# remove images
docker rmi gvcn/pangolin gvcn/pangolin:v3.1.11 pangolin
# pull from dockerhub
docker pull gvcn/pangolin
# test it
docker run --rm -ti gvcn/pangolin pangolin --help
docker run --rm -ti gvcn/pangolin pangolin -v
docker run --rm -ti gvcn/pangolin pangolin -pv
docker run --rm -v /your/data/dir:/data gvcn/pangolin pangolin <options>
```