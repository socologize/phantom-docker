The beginning...

1. Start your container.

      - docker run -it -d --privileged -v /sys/fs/cgroup:/sys/fs/cgroup:ro --name phantosd --hostname phantosd -p "80:80" -p "443:443" centos/systemd

2. Enter your container and run the commands. (docker exec -it phantosd /bin/bash)


      - yum update
      - rpm -Uvh https://repo.phantom.us/phantom/4.1/base/6/x86_64/phantom_repo-4.1.94-1.x86_64.rpm
      - /opt/phantom/bin/phantom_setup.sh install
      
 3. ???
 
 4. PROFIT!
 
 
 Note: You NEED a phantom login, so you can download and install the software. This is a pretty crappy way to make it, it's unoffical, and I will eventually improve it. You can start and stop the container as normal and everything fires back up just fine.  