# docker-manage-this-node

Dockerfile for [manage-this-node](https://github.com/onedr0p/manage-this-node)

## To use:
1. Install [Docker](https://www.docker.com/)

2. Clone the repo and build:

```
git clone https://github.com/chimpchimp/docker-manage-this-node.git
cd docker-manage-this-node
docker build -t chimpchimp/manage-this-node .
```
3. Make a directory to store the config file and copy the template from the orginal repo, naming it config.json.

4. Run the container, pointing to the directory with the config file:
```
docker run -d -p 3000:3000 \
--name="manage-this-node" \
-v <path to config folder>:/config \
--restart="always" \
chimpchimp/manage-this-node
```
