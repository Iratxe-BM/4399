```bash
#!/bin/sh
sudo yum update -y
sudo amazon-linux-extras install docker -y
sudo systemctl enable docker
sudo systemctl start docker
sudo docker container run --publish 80:8080 --name api --restart unless-stopped --detach secobau/4399-api
# sudo docker container exec -ti api sh
# curl FPFISSUPP-4399-API-4fa21df44bb55ee8.elb.eu-central-1.amazonaws.com:8080/C9/
```
