# prune-gcr
![Tests](https://github.com/expo/prune-gcr/workflows/Tests/badge.svg)

A little script to prune old Docker images from the Google Container Registry.

## Running the script

The script requires Python 2.7. You can run it with `./prune-gcr --project <project> <repository>`. If `--project` is not specified, it will attempt to infer the default project from your gcloud configuration.

```
usage: prune-gcr [-h] [--project PROJECT] [--older-than CUTOFF]
                 [--keep-at-least N]
                 repository

Prune old Docker images from the Google Container Registry. Example usage:
prune-gcr www

positional arguments:
  repository           short name of the GCR image repository (as in:
                       gcr.io/<project>/<repository>)

optional arguments:
  -h, --help           show this help message and exit
  --project PROJECT    name of the Google Cloud project. Defaults to
                       the project in your gcloud configuration.
  --older-than CUTOFF  prune images older than CUTOFF. Must be formatted as
                       YYYY-MM-DD. Uses GCP's time zone. Defaults to 90 days
                       ago.
  --keep-at-least N    keep at least N images, even if they are older than the
                       cutoff date. Defaults to 50.
```
