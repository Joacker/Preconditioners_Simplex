FROM ubuntu:latest


RUN apt-get update && apt-get install -y \
    bash \
    g++ \
    gcc \
    flex \
    bison \
    python2-dev \
    make \ 
    git \
    build-essential \
    cmake 

RUN apt install -y \
     python-is-python3

RUN apt install libeigen3-dev -y

#RUN apk add --update alpine-sdk

RUN apt update
RUN apt upgrade -y

# Continue with your Dockerfile instructions
WORKDIR /app
COPY ./ibex-lib-master /app

RUN chmod +x waf

# RUN ./waf configure --interval-lib=gaol --lp-lib=soplex \
# && ./waf install

CMD ["tail", "-f", "/dev/null"]

# ./__build__/src/ibexopt benchs/optim/medium/alkylbis.bch --random-seed=1
# ./waf distclean

# Mantener el contenedor en ejecución
# CMD ["tail", "-f", "/dev/null"]