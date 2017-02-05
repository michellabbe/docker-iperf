[![Docker Stars](https://img.shields.io/docker/stars/mlabbe/iperf.svg)](https://hub.docker.com/r/mlabbe/iperf/) [![Docker Pulls](https://img.shields.io/docker/pulls/mlabbe/iperf.svg)](https://hub.docker.com/r/mlabbe/iperf/)

# docker: iperf

This is a Docker image to run the [iperf](http://sourceforge.net/projects/iperf/) commandline tool in server mode for benchmarking network performance.

```sh
------------------------------------------------------------
Client connecting to speedtest.mydomain.local, TCP port 5001
TCP window size:  208 KByte (default)
------------------------------------------------------------
[  3] local 192.168.1.100 port 53912 connected with 192.168.1.50 port 5001
[ ID] Interval       Transfer     Bandwidth
[  3]  0.0-10.0 sec  1.10 GBytes   941 Mbits/sec
```

- Runs as non-root user
- Small image size
- Small number of layers

Total size of this image is only:

[![](https://images.microbadger.com/badges/image/mlabbe/iperf.svg)](https://microbadger.com/images/mlabbe/iperf)

________________________________________
### Pulling from Docker hub
If you want to obtain the image from Docker registry, you can use the following command:
```sh
docker pull mlabbe/iperf
```
________________________________________
### Running the image
In order to run the iperf server, use the following:
```sh
docker run --restart=unless-stopped --name=iperf -d -p 5001:5001 mlabbe/iperf
```
At that point, you can use your Docker server as an iperf server to begin
benchmarking your network speeds.
