# syntax=docker/dockerfile:1
FROM debian:12
WORKDIR /usr/share/app
COPY guestbook_python .
RUN apt-get update && apt-get install -y python3-pip  && apt-get clean && rm -rf /var/lib/apt/lists/*
ENV DB_REDIS redis
RUN pip3 install --no-cache-dir --break-system-packages -r requirements.txt
EXPOSE 3000
CMD python3 app.py