FROM python:3-alpine
WORKDIR /usr/src/app
RUN pip install --no-cache-dir tweepy
COPY . .
CMD [ "python", "./twitter_search.py" ]
