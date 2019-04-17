FROM ubuntu:16.04

WORKDIR /curler
COPY curler.sh .
RUN chmod +x ./curler.sh
RUN apt-get update && apt-get install -y curl
ENTRYPOINT ["./curler.sh"]
