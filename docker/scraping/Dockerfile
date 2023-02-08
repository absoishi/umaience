FROM python:3

RUN apt-get update && apt-get install -y locales && \
    localedef -f UTF-8 -i ja_JP ja_JP.UTF-8
ENV LANG ja_JP.UTF-8
ENV LANGUAGE ja_JP:ja
ENV LC_ALL ja_JP.UTF-8
ENV TZ JST-9
ENV TERM xterm

WORKDIR /app
COPY docker/scraping/requirements.txt .
RUN pip install -r requirements.txt
COPY src/scraping/ /app/