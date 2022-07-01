how-to
******

#copy source from windows host and log in linux system
------------------------------------------------------

pscp * root@10.203.21.131:/var/tmp

cd /var/tmp


#build an image from Dockerfile
-------------------------------

docker build -t hello-docker .

#or

docker build -t stephrey_node:1.0 .


#run the container
------------------

#it's maeby necessery to restart the deamon !

docker run hello-docker

#or

docker run stephrey_node:1.0


#list all images
----------------

docker images -a


#remove dangling images
-----------------------

docker images --filter "dangling=true"

docker rmi $(docker images -q --filter "dangling=true")


EOF