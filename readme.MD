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

## After docker compose up -d

### Daftar queue RabbitMQ ( wajibt tambahin di web setelah docker compose up -d)

```

- delete-cache-queue
routingKey: delete-cache
exchange: scoring-quiz-query

- quiz.email.queue


- scoringQuizQueryQueue
routingKey: correct-answer
exchange: scoring-quiz-query

- userAnswerQueue
routingKey: user-answer
EXCHANGE_NAME: quiz-command-quiz-query

```


### install curl di dkron 
````
docker exec -it ququiz-dkron sh
apk add curl
````

