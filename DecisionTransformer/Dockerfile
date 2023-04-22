FROM --platform=linux/x86_64 tensorflow/tensorflow:2.11.0-gpu

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get -y install \
    git \
    vim \
    && rm -rf /var/lib/apt/lists/*

COPY requirements.txt .
RUN pip --no-cache-dir install -r requirements.txt

COPY . .

CMD [ "bash" ]