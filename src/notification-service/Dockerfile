FROM python:3.11-alpine

# RUN apt-get update && apt-get install -y --no-install-recommends --no-install-suggests build-essential libpq-dev python3-dev ffmpeg && pip install --no-cache-dir --upgrade pip
RUN apk add --no-cache build-base libpq-dev ffmpeg
WORKDIR /app
COPY ./requirements.txt /app

RUN pip install --no-cache-dir --requirement /app/requirements.txt
COPY . /app

CMD ["python", "consumer.py"]