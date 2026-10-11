FROM rayproject/ray:2.56.1-py312-cu129-aarch64

USER root

COPY images/ray-cpu/requirements.txt /tmp/requirements.txt

RUN pip install --no-cache-dir \
    -r /tmp/requirements.txt

RUN pip3 install torch torchvision --index-url https://download.pytorch.org/whl/cu129

WORKDIR /app

USER ray

CMD ["ray", "start", "--block"]