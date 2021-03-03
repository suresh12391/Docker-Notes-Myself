#### Docker Build:

```
docker build . -f docker/Dockefile -t my-rails-app:latest
docker build --tag bulletinboard:1.0 .
docker build -t yourusername/example-node-app .
docker run --publish 8000:8080 --detach --name bb bulletinboard:1.0
docker stop bulletinboard
docker rm --force bulletinboard
```

```
docker login a.b.com
docker push a.b.com/test-repo:latest 
docker tag yourusername/example-node-app yourdockerhubusername/example-node-app:v1
docker logout  harbor.hinagro.com

docker pull debian:jessie
docker pull myregistry.local:5000/testing/test-image
```

###### Docker Registry Setup(ECR):
Note: This needs `awscli` to be installed. Execute: `sudo pip install awscli`
```
aws configure
aws ecr get-login (For the next docker login cmd)
aws ecr get-login-password --region ap-south-1 
docker login --username AWS XXXXX.ecr.ap-south-1.amazonaws.com => Supply password => Should Say Login Successful
```

##### Tagging:
```
docker tag SOURCE_IMAGE[:TAG] TARGET_IMAGE[:TAG]
docker tag bulletinboard:1.0 641305384395.dkr.ecr.ap-south-1.amazonaws.com/bulletinboard:latest
```

##### Push Images:
```
docker push TARGET_IMAGE[:TAG]
docker push XXXXX.ecr.ap-south-1.amazonaws.com/bulletinboard:latest
```

##### Pull Images:
docker pull XXXXX.ecr.ap-south-1.amazonaws.com/bulletinboard:latest

##### Delete Images:
aws ecr delete-repository --repository-name bulletinboard --region ap-south-1 --force



##### Image Push Note:
1) Create AWS ECR in the portal 
2) Create the Access key & Secret key in AWS portal
3) aws configure
4) aws ecr get-login-password --region {YOUR_REGION}
5) docker login --username AWS XXXXX.ecr.ap-south-1.amazonaws.com => Supply password => Should Say Login Successful
6) docker tag {SOURCE_IMAGE}:{TAG} {TARGET_IMAGE}:{TAG}
7) docker push {TARGET_IMAGE}:{TAG}
8) docker pull docker pull XXXXX.ecr.ap-south-1.amazonaws.com/{TARGET_IMAGE}:{TAG}


