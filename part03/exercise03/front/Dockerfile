FROM ubuntu:16.04

EXPOSE 5000

WORKDIR /mydir
RUN apt-get update && apt-get install -y git curl && \
curl -sL https://deb.nodesource.com/setup_10.x | bash && \
apt-get install -y nodejs && \
git clone https://github.com/docker-hy/frontend-example-docker.git && \
cd /mydir/frontend-example-docker && \
npm install && \
apt-get purge -y --auto-remove curl git && \
rm -rf /var/lib/apt/lists/* && \
useradd -m app && \
chown -R app /mydir

USER app
WORKDIR /mydir/frontend-example-docker
CMD API_URL=http://localhost:8000  npm start
