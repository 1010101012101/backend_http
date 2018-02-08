# backend_http
## EC2 Info
- Use SSH (another socket protocol like http) to directly access our EC2. Our EC2 has **public IP : 34.204.7.160**
``` 
ssh -i path_to_key ubuntu@34.204.7.160
``` 
- For example 
```
ssh -i Desktop/cs4400/cs4400_ec2_key.pem ubuntu@34.204.7.160
```
- type ```sudo su```
- To exit from the EC2 terminal and go back to your own type "exit".
## NGINX
- For a beginner **nginx** walkthrough go here: http://nginx.org/en/docs/beginners_guide.html
- For more help starting/stopping/restarting nginx go here: https://www.nginx.com/resources/wiki/start/topics/tutorials/commandline/
- nginx has one master process and several worker processes. The main purpose of the master process is to read and evaluate configuration, and maintain worker processes. Worker processes do actual processing of requests. nginx employs event-based model and OS-dependent mechanisms to efficiently distribute requests among worker processes. The number of worker processes is defined in the configuration file and may be fixed for a given configuration or automatically adjusted to the number of available CPU cores
- To start nginx, run the executable file.
```
sudo nginx
```
- Once nginx is started, it can be controlled by invoking the executable with the -s parameter. Use the following syntax:
```
nginx -s signal
```
- Where signal may be one of the following:
```stop``` fast shutdown
```quit``` graceful shutdown
```reload``` reloading the configuration file
```reopen``` reopening the log files
sudo nano /ect

## Node.js
- node.js runs javascript on the terminal (shell)
- To get yarn on server
``` 
npm instal -g yarn
```

- you have to tell it that http is allowed 

- to upadate code get to root directory then do
```
git pull
```
```npm run dist```  (compiled down version that can run on a node.js server)
```
server dist
```
- you need two sesssions that are always running (one for the node and one for the flask rest API) using an application called screen 

