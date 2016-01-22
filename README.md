# docker-manage-this-node

Dockerfile for [manage-this-node](https://github.com/onedr0p/manage-this-node)

## To use:
1. Install [Docker](https://www.docker.com/)

2. Make a directory to store the config file and copy the template from the orginal repo, naming it config.json.

3. Run the container, pointing to the directory with the config file. This should now pull the image from Docker hub:
  ```
  docker run -d -p 3000:3000 \
  --name="manage-this-node" \
  -v <path to config folder>:/config \
  --restart="always" \
  chimpchimp/manage-this-node
  ```
## Port Conflicts
If you run into a port conflict trying to run on 3000, for example if you're running [Plex Requests](https://github.com/lokenx/plexrequests-meteor), it is simple to modify the port forwarding:

`-p 3001:3000`
