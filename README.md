# docker-lab

A docker/docker-compose wrapper to quickly manage test containers.


### Dependencies

The script needs [Typer](https://github.com/tiangolo/typer), which can be
installed with `pip install -r requirements.txt`.

`docker` and `docker-compose` must be available.

### Usage

Containers from the `docker-compose.yml` in the `containers` subfolders will be created
with `docker-lab {foldername} up`, for example: `docker-lab debian up`.

To get access to a shell in the newly created container, type `docker-lab
{foldername} shell`.

Commands available for every container: `up`, `down`, `reset`, `shell`, `exec`, `cp`,
`info` and `stop`. The flag `--help` can be used after a command to get more
information about it.

With `docker-lab ps` the status of every managed container can be seen.


### Add a new container

Simply create a `containers` subfolder, naming it as desired.

In there, put a `docker-compose.yml`, using the already existing one as template.

Keep the name of the service equals to the one of the folder.
