# Install Kata Containers on Ubuntu

1. Install the Kata Containers components with the following commands:

   ```bash
   $ ARCH=$(arch)
   $ sudo sh -c "echo 'deb https://download.opensuse.org/repositories/home:/katacontainers:/releases:/${ARCH}:/master/xUbuntu_$(lsb_release -rs)/ /' > /etc/apt/sources.list.d/kata-containers.list"
   $ curl -sL  https://download.opensuse.org/repositories/home:/katacontainers:/releases:/${ARCH}:/master/xUbuntu_$(lsb_release -rs)/Release.key | sudo apt-key add -
   $ sudo -E apt-get update
   $ sudo -E apt-get -y install kata-runtime kata-proxy kata-shim
   ```

2. Decide which container manager to use and select the corresponding link that follows:

   - [Docker](docker/ubuntu-docker-install.md)
   - [Kubernetes](https://github.com/kata-containers/documentation/blob/master/Developer-Guide.md#run-kata-containers-with-kubernetes)
