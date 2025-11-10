FROM ubuntu:20.04

RUN apt update && apt install -y \
    libgmp-dev \
    libmpfr-dev \
    libmpc-dev \
    python3.8 \
    python3-pip \
    python3-gmpy2 \
    build-essential

WORKDIR /app

COPY . . 

RUN pip3 install -r requirements.txt

ADD entrypoint.sh /
ENTRYPOINT ["/entrypoint.sh"]
