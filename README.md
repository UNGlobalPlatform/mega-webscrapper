# Mega Webscrapper, Apache NiFi, Tika and OpenNLP

Mega website scrapper, using Apache NiFi, OpenNLP and Apache Tika.

![Apache NiFi/Mega Webscraper](https://github.com/UNGlobalPlatform/mega-webscrapper/blob/master/docs/nifi-mega-webscraper.png?raw=true)

## Getting Started

## Prerequisites

For this part we are going to need;

* AWS Instance with minimum of 2GB of memory and 50GB of disk space
* Required NAR files for the additional OpenNLP and URL Extractor
* AWS Access key, with permissions to read/write to AWS S3

### Required NAR Files

OpenNLP

ExtractText

### Required NiFi Controller Services

#### AWSCredentialsProviderControllerService

https://nifi.apache.org/docs/nifi-docs/components/org.apache.nifi/nifi-aws-nar/1.3.0/org.apache.nifi.processors.aws.credentials.provider.service.AWSCredentialsProviderControllerService/index.html

#### DistributedMapCacheClientService

https://nifi.apache.org/docs/nifi-docs/components/org.apache.nifi/nifi-distributed-cache-services-nar/1.3.0/org.apache.nifi.distributed.cache.client.DistributedMapCacheClientService/index.html

#### DistributedMapCacheServer

https://nifi.apache.org/docs/nifi-docs/components/org.apache.nifi/nifi-distributed-cache-services-nar/1.3.0/org.apache.nifi.distributed.cache.server.map.DistributedMapCacheServer/index.html

## Installation

### Java Heap Size

Bootstrap.conf file:

The bootstrap.conf file in the conf directory allows users to configure settings for how NiFi should be started. This includes parameters, such as the size of the Java Heap, what Java command to run, and Java System Properties. This files comes pre-configured with default values.
```
java.arg.2=-Xms512m
java.arg.3=-Xmx512m
```
![Apache NiFi/Java Heap Size](https://github.com/UNGlobalPlatform/mega-webscrapper/blob/master/docs/nifi-javahelp.png?raw=true)

This section is used to control the amount of heap memory to use by the JVM running NiFi. Xms defines the initial memory allocation, while Xmx defines the maximum memory allocation for the JVM. As you can see the default values are very small and not suitable for dataflows of any substantial size.

Increase both the initial and maximum heap memory allocations to at least 4GB or 8GB for starters, or else the scraper will run out of memory.

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Authors

* **Mark Craddock** - *Initial work*
* **Neville de Mendonca** - *Initial work*

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

TBD

## Acknowledgments

https://nifi.apache.org/docs/nifi-docs/html/administration-guide.html
https://tika.apache.org/

