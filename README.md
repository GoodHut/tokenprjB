# tokenprjB
nate158@nate158.net
version: '3' 

 services: 

   netdata: 

     image: netdata/netdata 

     container_name: netdata 

     # set to fqdn of host 

     hostname: My Server Aliyun 

     ports: 

       - 19999:19999 

     restart: unless-stopped 

     cap_add: 

       - SYS_PTRACE 

     security_opt: 

       - apparmor:unconfined 

     volumes: 

       - netdataconfig:/etc/netdata 

       - netdatalib:/var/lib/netdata 

       - netdatacache:/var/cache/netdata 

       - /etc/passwd:/host/etc/passwd:ro 

       - /etc/group:/host/etc/group:ro 

       - /proc:/host/proc:ro 

       - /sys:/host/sys:ro 

       - /etc/os-release:/host/etc/os-release:ro 

  

 volumes: 

   netdataconfig: 

   netdatalib: 

   netdatacache:...
