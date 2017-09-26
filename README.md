# Mega Webscrapper, Apache NiFi, NLP, OpenNLP

Mega website scrapper, using Apache NiFi, OpenNLP and Apache xxxx to extract text from documents.

![Apache NiFi/Mega Webscraper](https://github.com/UNGlobalPlatform/mega-webscrapper/blob/master/docs/nifi-mega-webscraper.png?raw=true)

## Getting Started

## Prerequisites

For this part we are going to need xxxx.

### Required NAR Files

NLP

NLP Core


AWS Credentials Service

DistributedMapCacheClientService

### Required NiFi Controller Services

#### AWSCredentialsProviderControllerService

https://nifi.apache.org/docs/nifi-docs/components/org.apache.nifi/nifi-aws-nar/1.3.0/org.apache.nifi.processors.aws.credentials.provider.service.AWSCredentialsProviderControllerService/index.html

#### DistributedMapCacheClientService

https://nifi.apache.org/docs/nifi-docs/components/org.apache.nifi/nifi-distributed-cache-services-nar/1.3.0/org.apache.nifi.distributed.cache.client.DistributedMapCacheClientService/index.html

#### DistributedMapCacheServer

https://nifi.apache.org/docs/nifi-docs/components/org.apache.nifi/nifi-distributed-cache-services-nar/1.3.0/org.apache.nifi.distributed.cache.server.map.DistributedMapCacheServer/index.html

## Installation

### Java Heap Size
Increase the java heap size, or else the scraper will run out of memory. Change the following to suite the memory within your server.

```
java.arg.2=-Xms512m
java.arg.3=-Xmx512m
```

![Apache NiFi/Java Heap Size](https://github.com/UNGlobalPlatform/mega-webscrapper/blob/master/docs/nifi-javahelp.png?raw=true)


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
