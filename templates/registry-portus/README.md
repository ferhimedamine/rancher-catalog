# Rancher Registry with Portus UI

It is a fork from community catalog [Registry](https://github.com/rancher/community-catalog/tree/master/templates/registry). Read the original readme for more details.

This catalogue item have several modifications from the original to make it have more compatibility and configurable options.

## External load balancer and https termination

LB service and sslproxy service is removed from original, you should setup your own load balancer that do the routing and terminate it with https.

For example, you can setup rancher-lb for routing and rancher-letsencrypt to obtain certificates for https termination.
- For portus routing, you should route to port 3000 of the portus services
- For registry routing, you should route to port 5000 of the registry services

### Rancher active proxy Support

Support configuration of [adi90x/rancher-active-proxy](https://github.com/adi90x/rancher-active-proxy)

## More recent portus image and mariadb

Using recent portus image that built from official and using mariadb instead of mysql.

## Added S3 storage backend compatibility to registry service

Allow using Amazon S3 as a storage backend for the registry.

## Automatically generated certificates for registry authentication with portus

For registry authentication with portus, ssl certificates is needed to encrypt the content. Since it is only used for data encryption, a self-signed is used instead. This catalog use paulczar/omgwtfssl to generate the ssl certificates.

## Different domain for portus and registry

Allow having different domain for portus and registry service.

## Support SMTP server for portus mail notification

Allow Portus to send mail notification using SMTP.
