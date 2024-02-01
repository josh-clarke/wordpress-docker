# wordpress-docker
Docker Compose file to spin up a fresh container to locally develop a Wordpress site, theme, or plugin.

## Quick Start

You need [Docker](https://docs.docker.com/desktop/) installed on your computer for this to work.

1. Clone this repo or download the zip file
2. Enter the repo folder or extract the zip file
3. Copy `docker-compose.yml` to the local project folder for your Wordpress project
4. Open a terminal and navigate to your project directory
5. Type the command `docker compose docker-compose.yml`

When Docker has finished setting up your Wordpress site, it will be available to view on http://localhost. The folders for the Wordpress Themes will be available in your project folder under `./themes` and the Wordpress plugins folder will be availalble under `./plugins`. The MySQL database files will be available in the `./mysql` folder.

## Advanced Setup

There are several things you can do to customize the `docker-compse.yml` for your setup.

1. **Change the port on your computer where you will view your Wordpress site.** Sometimes you want to view a site on a port other than the default, so if you change the first port number under `wp:` > `ports:80:80` to another number, say 8080 (`ports:8080:80`), you can view your dev site at http://localhost:8080/
2. **Change the name of your containers by modifying the `container_name` value.** This is mostly for your own reference if you are running several container environments in Docker
3. **Change the database users or passwords by modifying the values under `environment` in both containers.** If you are running this on your own workstation, this is probably not necessary.

There are more things you can do that can be discovered with a little searching, such as using a MariaDB container or using another version of Wordpress rather than the latest.