
```
kubectl autoscale deployment health-app-deploy --cpu-percent=120 --min=3 --max=10 -n my-team-1001

# slowly add stress
sudo docker run --rm williamyeh/wrk:4.0.2 -c2 -d30s --latency  http://35.192.144.224:32003/api/v1.0/add/cpu_load 
sudo docker run --rm williamyeh/wrk:4.0.2 -c3 -d45s --latency  http://35.192.144.224:32003/api/v1.0/add/cpu_load 
sudo docker run --rm williamyeh/wrk:4.0.2 -c5 -d45s --latency  http://35.192.144.224:32003/api/v1.0/add/cpu_load 
sudo docker run --rm williamyeh/wrk:4.0.2 -c8 -d60s --latency  http://35.192.144.224:32003/api/v1.0/add/cpu_load  
```
