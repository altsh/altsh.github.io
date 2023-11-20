# note

## cmd

```sh
# on wsl
docker pull httpd
docker run --rm -it -v ~/wsl/altwiz.github.io/docs:/usr/local/apache2/htdocs -w /usr/local/apache2/htdocs -p 8080:80 httpd bash

docker pull node
cat ~/wsl/Dockerfile/pug
FROM node
RUN npm install --global pug-cli
docker build -t pug -f ~/wsl/Dockerfile/pug .
docker run --rm -it -v ~/wsl:/wsl -w /wsl pug bash
cd /wsl/pug
pug src/ --out docs/
cp src/*.css docs/
```