# Jupyter Notebook for Copernicus Sentinel Analysis

Jupyter notebook with support for geospatial analyses. Everything what gives [Jupyter Notebook Scientific Python Stack](https://github.com/jupyter/docker-stacks/tree/master/scipy-notebook) and more:

* [GDAL](http://www.gdal.org/)
* [Sentinelsat](https://github.com/sentinelsat/sentinelsat)

## Basic Use

The following command starts a container with the Notebook server listening for HTTP connections on port 8888 with a randomly generated authentication token configured. Current folder is mapped to the server.

```bash
docker run -it --rm -p 8888:8888 -v $PWD/:/home/jovyan krostir/jupyter-geo-sentinel
```

One can optionally provide the [Copernicus Open Access Hub] <https://scihub.copernicus.eu/> username and password.

```bash
docker run -it --rm -p 8888:8888 -v $PWD/:/home/jovyan  -e SentinelHub_UN='[SentinelHub user name]' -e SentinelHub_PASS='[SentinelHub password]' krostir/jupyter-geo-sentinel
```

Take note of the authentication token included in the notebook startup log messages. Include it in the URL you visit to access the Notebook server or enter it in the Notebook login form.

For all other options see [jupyter/docker-stacks](https://github.com/jupyter/docker-stacks).