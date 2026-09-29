FROM rayproject/ray:2.56.1-py311

USER root

COPY images/ray-cpu/requirements.txt /tmp/requirements.txt

RUN pip install --no-cache-dir \
    -r /tmp/requirements.txt

WORKDIR /app

USER ray

CMD ["ray", "start", "--block"]