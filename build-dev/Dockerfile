FROM python:3.6
LABEL maintainer 'Jefferson Pantoja'

RUN useradd www && \
    mkdir /app && \
    mkdir /log && \
    chown www /log && \
    chown www /app

USER www
VOLUME /log
WORKDIR /app
EXPOSE 8000

COPY index.html /app
COPY run.py /app
ENTRYPOINT ["/usr/local/bin/python"]
CMD ["run.py"]