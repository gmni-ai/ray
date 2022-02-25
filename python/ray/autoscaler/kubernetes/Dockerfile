FROM rayproject/ray:nightly-py38

RUN pip install transformers torch sentencepiece

RUN wget -q https://github.com/prometheus/prometheus/releases/download/v2.26.0/prometheus-2.26.0.linux-amd64.tar.gz
RUN tar xvfz prometheus-2.26.0.linux-amd64.tar.gz
RUN mv prometheus-2.26.0.linux-amd64 prometheus
COPY prometheus.yaml .
COPY defaults.yaml anaconda3/lib/python3.8/site-packages/ray/autoscaler/kubernetes/defaults.yaml
