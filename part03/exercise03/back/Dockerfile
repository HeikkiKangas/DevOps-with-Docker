FROM ubuntu:16.04

EXPOSE 8000

WORKDIR /mydir
RUN apt-get update && apt-get install -y git curl && \
curl -sL https://deb.nodesource.com/setup_10.x | bash && \
apt-get install -y nodejs && \
git clone https://github.com/docker-hy/backend-example-docker.git && \
cd /mydir/backend-example-docker && \
npm install && \
apt-get purge -y --auto-remove curl git && \
rm -rf /var/lib/apt/lists/* && \
useradd -m app && \
chown -R app /mydir

USER app
WORKDIR /mydir/backend-example-docker
CMD FRONT_URL=http://localhost:5000  npm start
