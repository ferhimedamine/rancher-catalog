# GitLab CE

It is a catalog entry of [sameersbn/docker-gitlab](https://github.com/sameersbn/docker-gitlab).

## Load balancer

### Rancher active proxy support

Support configuration of [adi90x/rancher-active-proxy](https://github.com/adi90x/rancher-active-proxy)

### Other load balancer

Any load balancer that does not require additional configuration on backend services, otherwise you need to fork this template.

## SSH Port mapping

By default, a gitlab container instance need to map a port on host for SSH connection. If you want to load balance it in backend without mapping the SSH port on host, you need to fork this template.
