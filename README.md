## Installation

Build/run this container:
```sh
docker-compose create
docker-compose up -d
```


## Running test

Enter to container:
```sh
docker ps -a
docker exec -it [container_id] /bin/bash
```

Test speed:
```sh
cd /var/www
time dd if=/dev/zero of=test.dat bs=1024 count=50000
rm -rf test.dat
cd /tmp
time dd if=/dev/zero of=test.dat bs=1024 count=50000
rm -rf test.dat
```

Remove container
```sh
docker rm [container_id] -f
docker rmi phusion/baseimage:0.9.19
```


## Additional information

### Results on mac

Speed of write to volume:
`
real	0m40.111s
user	0m0.400s
sys	0m4.430s
`

Speed of write to docker write layer:
`
real	0m0.520s
user	0m0.050s
sys	0m0.460s
`




