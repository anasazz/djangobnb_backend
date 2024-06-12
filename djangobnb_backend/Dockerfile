FROM python:3.12.2-slim-bullseye

WORKDIR /Users/macbookm1/Documents/NextDjango/djangobnb_backend/djangobnb_backend

ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

RUN apt-get update && apt-get install -y netcat

RUN pip install --upgrade pip
COPY ./requirements.txt .
RUN pip install -r requirements.txt

COPY ./entrypoint.sh .
RUN sed -i 's/\r$//g' /Users/macbookm1/Documents/NextDjango/djangobnb_backend/djangobnb_backend/entrypoint.sh
RUN chmod +x /Users/macbookm1/Documents/NextDjango/djangobnb_backend/djangobnb_backend/entrypoint.sh

COPY . .

ENTRYPOINT [ "/Users/macbookm1/Documents/NextDjango/djangobnb_backend/djangobnb_backend/entrypoint.sh" ]