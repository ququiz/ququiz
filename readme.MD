# Ququiz Microservices

#### setup ci/cd jenkins docker compose 
```
:)
(yg di docs, gakbisa jalanin docker yg di localhost)
Setup CI jenkins docker compose:
-- setup
cd scalable
docker image build -t myjenkins .

docker create volume jenkins_home

docker run -it -d --name jenkins-blueocean -p 9080:8080 -p 50000:50000 -v /var/run/docker.sock:/var/run/docker.sock -v jenkins_home:/var/jenkins_home myjenkins


docker exec -i -t jenkins-blueocean sh
docker login 
```


