# syntax=docker/dockerfile:1
FROM debian:12
WORKDIR /usr/share/app
COPY guestbook_python .
ENV DB_REDIS redis
RUN pip3 install --no-cache-dir --break-system-packages -r requirements.txt
EXPOSE 3000
CMD python3 app.py