This Docker image does a few things.

** Installs Tomcat 8
** Copies tomcat-users.xml to Tomcat's conf directory
** Copies JRebel agent files to the correct directory
** Installs bash


Things you need to do manually before you run this image.

** Either buy or get a trial license of JRebel
** Activate JRebel
** Follow the instruction to obtain the libjrebel64.so and jrebel.jar file.  Files should be copied to directory of the Dockerfile.

To build the Dockerfile

docker build -t [name of image] -f Dockerfile .

To run the image after it is built, you can run the command below.  This is running in attached mode.

docker run -dit --rm -p 8080:8080 [name of image]

Now that the image is running.  You should be able to access the Tomcat manager with the credentials of tomcat/s3cret.

http://localhost:8080/manager/html






