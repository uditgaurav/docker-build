FROM python:2.7-wheezy

# Install locust
RUN python -m ensurepip --upgrade && pip install locustio

ADD build/locustfile.py /config/locustfile.py
ADD build/runLocust.sh /usr/local/bin/runLocust.sh

ENV LOCUST_FILE /config/locustfile.py

EXPOSE 8089

ENTRYPOINT ["/usr/local/bin/runLocust.sh"]
