FROM python:3.11.7-slim

ENV PYTHONUNBUFFERED=1

WORKDIR /backend
COPY ./backend/requirements.txt requirements.txt
RUN python3 -m pip install -i https://pypi.tuna.tsinghua.edu.cn/simple/ -r requirements.txt

COPY ./backend .
COPY ./backend/conf/docker.py conf/env.py

CMD ["daphne", "-b", "0.0.0.0", "-p", "8000", "fuadmin.asgi:application"]
