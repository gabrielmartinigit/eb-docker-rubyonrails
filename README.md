# Ruby on Rails example - Elastic Beanstalk - GitHub Actions

## Geeting Started

**Executando o container local**

```
docker build -t rubyonrailstest .

docker run -d -p 8080:3000 rubyonrailstest

```

**Publicando a imagem no ECR**

```
aws ecr get-login-password --region us-east-1 | docker login --username AWS --password-stdin account-id.dkr.ecr.us-east-1.amazonaws.com

docker tag rubyonrailstest:latest account-id.dkr.ecr.us-east-1.amazonaws.com/rubyonrailstest:latest

docker push account-id.dkr.ecr.us-east-1.amazonaws.com/rubyonrailstest:latest
```

## Referências

- https://www.docker.com/resources/what-container
- https://www.youtube.com/playlist?list=PLf-O3X2-mxDkiUH0r_BadgtELJ_qyrFJ_
- https://docs.docker.com/samples/rails/
- https://hub.docker.com/_/ruby
- https://docs.aws.amazon.com/pt_br/elasticbeanstalk/latest/dg/docker.html
