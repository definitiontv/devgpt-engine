FROM python:3.11-slim


RUN apt-get update && apt-get install -y sudo tk tcl gcc curl nano git

WORKDIR /app

COPY . .
COPY docker/entrypoint.sh ./entrypoint.sh

RUN sudo pip install -e .
RUN pip install open-interpreter

ENTRYPOINT ["bash", "/app/entrypoint.sh"]
