This project provide docker image for sip-proxy.

To deploy the container use command below:
docker run --name sip-proxy -p 5060:5060/udp -p 7070-7080:7070-7080/udp -d leejoneshane/sip-proxy

Then, You must use console to change sip-proxy configure file (siproxd.conf), like:
docker exec -it sip-proxy bash

\#>vi /etc/siproxd.conf
\#>exit

When You finish this job, restart the container by:
docker restart sip-proxy
