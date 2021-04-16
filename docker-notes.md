docker run [args] image:tag [command] [args]

1. interactive session \
docker run -it centos bash

2. list all active or suspended containers \
docker ps -a

3. restart a container \
docker restart [containerID] \
docker attach [containerID]

4. kill a container \
docker kill [containerID] \
docker stop [containerID]

5. remove all suspended container \
docker rm $(docker ps -aq)

6. automatically remove container after exit:  *--rm* \
docker run -it *--rm* centos bash

7. share file between container and host OS: *-v* \
docker run -it --rm *-v* <mark>[host_path]:[container_path]</mark> image bash \
docker run -it --rm *-v* <mark>$(pwd)/tmp/test:/opt/ml</mark>  centos bash 

8. run in background (detached): *-d*
docker run -d image

9. port forwarding: *-p* \
docker run *-p* [hostport[]:[container_port] image \
docker run *-p* 8080:80 -d nginx 

10. pass environment variable: *-e*
docker run -it --rm -e MYSECRETE=NOSECRETE 


[Youtube link](https://www.youtube.com/watch?v=yrE2vJDcFVM&t=4s)


