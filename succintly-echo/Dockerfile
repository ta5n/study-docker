FROM ubuntu

RUN apt-get update && apt-get install -y netcat-openbsd

ENV LOG_FILE /server-logs/succintly-echo.log
S
COPY ./succintly-echo /usr/local/bin/succintly-echo

RUN chmod +x /usr/local/bin/succintly-echo

EXPOSE 8082

VOLUME /server-logs

CMD ["succintly-echo", "--port", "8082"]