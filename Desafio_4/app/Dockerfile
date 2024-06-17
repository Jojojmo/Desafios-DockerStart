FROM python:3.11-slim

WORKDIR /app

#RUN apt-get update && apt-get install -y redis-server

ENV FLASK_APP=app.py
ENV FLASK_RUN_HOST=0.0.0.0

#RUN apk add --no-cache gcc musl-dev linux-headers

COPY requirements.txt requirements.txt

RUN pip install --upgrade pip && \
pip install -r requirements.txt

EXPOSE 5000

COPY . .

CMD ["flask", "run"]
