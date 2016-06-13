# Apache Nutch 2 Docker Image (with HBase as storage layer) 

Apache Nutch is a highly extensible and scalable open source web crawler software project. HBase is a fast storage layer that serves Nutch to keep all the links to crawl.

## Installation

```
docker build --rm=true -t cogfor/nutch:2.3.1 .
```

## Usage

Modify `conf/nutch-site.xml` to define a crawler and configure storage

## Volume mounting

You may want to mount a local volume:

```
docker run -it -v conf:/nutch-source/conf -v /data cogfor/nutch:2.3.1 
```

# Notes

Although we use Apache HBase as our default storage, you are not limited in doing so. This image can be used independently of the supplied Standalone HBase install.
