FROM python:3.6

RUN python3 -m pip install -U pip && python3 -m pip install -U setuptools &&  pip3 install locust

ADD build/locustfile.py /config/locustfile.py
ADD build/runLocust.sh /usr/local/bin/runLocust.sh

ENV LOCUST_FILE /config/locustfile.py

EXPOSE 8089

ENTRYPOINT ["/usr/local/bin/runLocust.sh"]
