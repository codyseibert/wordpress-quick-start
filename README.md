# Wordpress Docker Quick Start

The following repo is for hosting wordpress application on a ubuntu 20.04 virtual machine. I have successfully ran this script on a digital ocean droplet, but I assume this setup.sh script could be modified or used on any potential ubuntu VM host.

# Instructions

1. create a ubuntu 20.04 Digital Ocean droplet.
2. ssh into your droplet, i.e. `ssh root@127.127.127.127`
3. setup an A record which points your domain to the IP of your droplet (A blog.thewebdevjunkie.com => 127.127.127.127)
4. clone the repo `git clone https://github.com/codyseibert/wordpress-quick-start.git`
5. cd into the directory `cd wordpress-quick-start`
6. modify `.env` to replace your secret passwords
7. modify `Caddyfile` to have the domain or subdomain you expect to host your wordpress site
8. run the setup script: `./setup.sh`
9. load up a web browser to your domain (it might take a minute to host the database, wordpress, and Caddy, so give it some time)

## Credits

I followed the following documentation to figure out most of the necessary docker / caddy setup.

- https://minhcung.me/how-to-start-wordpress-with-caddy/
- https://docs.docker.com/engine/install/ubuntu/
- https://docs.docker.com/compose/install/
- https://docs.docker.com/samples/wordpress/
