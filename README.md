This Docker image does a few things.

1. Installs Tomcat 8
1. Copies tomcat-users.xml to Tomcat's conf directory
1. Copies JRebel agent files to the correct directory
1. Installs bash


Things you need to do manually before you run this image.

1. Either buy or get a trial license of JRebel
1. Activate JRebel
1. Follow the instruction to obtain the libjrebel64.so and jrebel.jar file.  1. Files should be copied to directory of the Dockerfile.

To build the Dockerfile

```
docker build -t [name of image] -f Dockerfile .
```

To run the image after it is built, you can run the command below.  This is running in attached mode.

```
docker run -it --rm -p 8080:8080 [name of image]
```

Now that the image is running.  You should be able to access the Tomcat manager with the credentials of tomcat/s3cret.

http://localhost:8080/manager/html


You can deploy manually or through a Maven plugin.  Once your application is deployed, the JRebel agent will push changes to Tomcat for you.  No need to redeploy.  JREBEL WILL DO IT FOR YOU!




