FROM ubuntu:22.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && \
    apt-get install -y \
      libgcc-s1 \
      libc6 \
    && rm -rf /var/lib/apt/lists/*

WORKDIR /app

COPY ./src/nom_prog /app/nom_prog

# Binaire exécutable
RUN chmod +x /app/nom_prog

CMD ["/app/nom_prog"]
