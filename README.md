# kali-linux-docker
Docker image for kali that fixes some repo issues with main image. May have modified to auto build Metasploit.

Also exposes port for shell handler or whatever needed on 443

Pull the image
-------

    docker pull lockfale/kali-linux-docker

	
Running
-------

    docker run -i -p 443:443 -t lockfale/kali-linux-docker
    
or my preference is to run in background daemon mode and attach to it (so I can detach later)

    docker run -p 443:443 -itd lockfale/kali-linux-docker
    docker ps |grep kali-linux-docker
    docker attach <container id>


If you do not need to run a handler, just remove the -p 443:443

    docker run -i -t digitalshokunin/kali-linux-docker



Why use Docker? [Pentesting with Docker](https://www.youtube.com/watch?v=gC_vm1wc-AY)

