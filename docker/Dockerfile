FROM python:3.9.5-buster

RUN pip install --upgrade pip

RUN adduser --disabled-login worker
USER worker
WORKDIR /home/worker

COPY --chown=worker:worker requirements.txt requirements.txt
RUN pip install --user -r requirements.txt

ENV PATH="/home/worker/.local/bin:${PATH}"

COPY --chown=worker:worker . .

# LABEL maintainer="Your Name <your-mail@example.com>" \
#       version="1.0.0"

# CMD ["python"]