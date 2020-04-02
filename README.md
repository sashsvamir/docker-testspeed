## Description

Docker benchmark of writes to volumes in "delegated" or "cached" modes.

See issues:
- https://docs.docker.com/docker-for-mac/osxfs/#performance-issues-solutions-and-roadmap
- https://github.com/docker/for-mac/issues/1592
- https://www.docker.com/blog/user-guided-caching-in-docker-for-mac/
- https://forums.docker.com/t/file-access-in-mounted-volumes-extremely-slow-cpu-bound/8076/264
- https://docs.docker.com/docker-for-mac/osxfs-caching/
- https://github.com/docker-library/postgres/issues/299


## Installation

- Download package:
```sh
git clone git@github.com:sashsvamir/docker-testspeed.git
cd docker-testspeed
```



## Running test

Just run and see results:
```sh
docker-compose up
docker-compose down
```



## Additional information


#### Results on mac

Default speed of write 10 MB to docker write to:
- layer:
```
....70.3 MB/s
real	0m0.148s
user	0m0.013s
sys	0m0.116s
```

- to volume:
```
....2.0 MB/s
real	0m5.225s
user	0m0.026s
sys	0m0.443s
```

#### To see states of osxfs:
```
/Applications/Docker.app/Contents/MacOS/com.docker.osxfs state
```

