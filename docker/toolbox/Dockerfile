FROM alpine
RUN apk add --no-cache curl wget busybox-extras netcat-openbsd bash
# python py-pip && \
#    pip install awscli
# Install python/pip
ENV PYTHONUNBUFFERED=1
RUN apk add --update --no-cache python3 && ln -sf python3 /usr/bin/python
RUN python3 -m ensurepip
RUN pip3 install --no-cache --upgrade pip setuptools awscli
RUN apk --purge -v del pip3
CMD tail -f /dev/null
