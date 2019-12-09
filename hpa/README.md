
```
sudo docker run --rm williamyeh/wrk:4.0.2 -c5 -d5s --latency  http://35.226.87.85:32003/api/v1.0/show/pod_name
sudo docker run --rm williamyeh/wrk:4.0.2 -c1 -d30s --latency  http://35.192.144.224:32003/api/v1.0/add/cpu_load 
sudo docker run --rm williamyeh/wrk:4.0.2 -c2 -d30s --latency  http://35.192.144.224:32003/api/v1.0/add/cpu_load 
sudo docker run --rm williamyeh/wrk:4.0.2 -c3 -d45s --latency  http://35.192.144.224:32003/api/v1.0/add/cpu_load 
sudo docker run --rm williamyeh/wrk:4.0.2 -c5 -d45s --latency  http://35.192.144.224:32003/api/v1.0/add/cpu_load 
sudo docker run --rm williamyeh/wrk:4.0.2 -c8 -d60s --latency  http://35.192.144.224:32003/api/v1.0/add/cpu_load  

```
