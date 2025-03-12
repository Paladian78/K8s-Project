FROM python:3.11-alpine

# RUN apt-get update && apt-get install -y --no-install-recommends --no-install-suggests build-essential libpq-dev python3-dev && pip install --no-cache-dir --upgrade pip
RUN apk add --no-cache build-base libpq-dev

WORKDIR /app
COPY ./requirements.txt /app

RUN pip install --no-cache-dir --requirement /app/requirements.txt
COPY server.py /app

EXPOSE 5000

CMD ["python", "server.py"]