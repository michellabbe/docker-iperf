# docker: iperf

This is a Docker image to run the [iperf](http://sourceforge.net/projects/iperf/) commandline tool for benchmarking network performance.

### Pulling from Docker hub
If you want to obtain the image from Docker registry, you can use the following command:
```
docker pull mlabbe/iperf
```
### Running the image
In order to run the iperf server, use the following:
```
docker run -d -p 5001:5001 mlabbe/iperf
```
At that point, you can use your Docker server as an iperf server to begin
benchmarking your network speeds.
