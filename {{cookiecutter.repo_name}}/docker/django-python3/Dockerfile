FROM base
MAINTAINER Egyed Zoltán "zoltan.egyed@vertis.com"
RUN groupadd -g 8000 django && useradd -u 8000 -g 8000 -m django

RUN set -x \
    && apt-get update \
    && DEBIAN_FRONTEND=noninteractive \
       apt-get install -y --no-install-recommends \
           libpq5 \
           libpython3.4 \
    && DEBIAN_FRONTEND=noninteractive \
       apt-get install -y --no-install-recommends \
           python3-pip \
           libpq-dev \
           build-essential \
           python3-dev \
           git \
    && pip3 install \
           uwsgi==2.0.12 \
           django==1.9.1 \
           psycopg2==2.6.1 \
           django-debug-toolbar==1.4 \
           django-rosetta==0.7.8