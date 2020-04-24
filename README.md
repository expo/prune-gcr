# prune-gcr

A little script to prune old Docker images from the Google Container Registry.

## Running the script

The script requires Python 2.7. You can run it with `./prune-gcr <repository>`. It will attempt to infer the default project from your gcloud configuration. If there is no default project or you wish to explicitly specify one, use the `--project` option.
