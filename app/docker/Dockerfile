FROM dustynv/cuda-python:r36.4.0-cu128-24.04

WORKDIR /usr/src/fastapi_app

COPY ../requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt

COPY .. ./app

# Ignore UserWarning (mobile_sam package)
ENV PYTHONWARNINGS=ignore

EXPOSE 8000
