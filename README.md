# Drone

Run [Drone CI](http://drone.io/) in a [Docker](http://docker.io/) container.

Link: [mattgruter/drone](https://registry.hub.docker.com/u/mattgruter/drone/)


## Setup
With newer versions of drone most of the configuration has been moved away from the UI and into drone's configuration file and/or environment variables. Use the `--env`/`-e` option to `docker run` to setup integration with your source control system (GitHub, Bitbucket, Gitlab, ...). Refer to [drone's configuration documentation](http://readme.drone.io/setup/config/settings/).

## Run
The drone image runs its own docker daemon within the container. This requires elevated privileges. Hence you must use the `--privileged` run flag.

## Example
With GitHub integration:

    docker run -e DRONE_GITHUB_CLIENT="..." -e DRONE_GITHUB_SECRET="..." -p 8080:80 --privileged mattgruter/drone

And point your browser to [http://localhost:8080](http://localhost:8080/).


