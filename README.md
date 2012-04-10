This is a simple DIY cartridge demo that illustrates the use of java in the
DIY application repo. The application consists of a single test.MyHttpServer main class that is located in the repository bin directory. The src for the class is in the src directory. To update the class run by the DIY cartridge you would simple recompile it using:

javac -g -d bin src/test/MyHttpServer.java

# First, create the DIY java application
Assuming you have an OpenShift account and domain setup, and client tools installed (if you don't, see https://openshift.redhat.com/app/getting_started), you create your DIY application using:

[8](ironmaiden:tmp) > rhc app create -t diy-0.1 -a diy -p *
Creating application: diy
Now your new domain name is being propagated worldwide (this might take a minute)...
    retry # 5 - Waiting for DNS: diy-jbossdev.rhcloud.com
Confirming application 'diy' is available:  Success!

diy published:  http://diy-jbossdev.rhcloud.com/
git url:  ssh://0baa01674cac4a96a8ef8a1096867680@diy-jbossdev.rhcloud.com/~/git/diy.git/
Disclaimer: This is an experimental cartridge that provides a way to try unsupported languages, frameworks, and middleware on Openshift.

# Second, pull replace your app repository with the java-demo contents
git remote add origin git@github.com:openshift/openshift-diy-java-demo.git
