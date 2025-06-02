FROM dustynv/l4t-pytorch:r36.4.0

WORKDIR /usr/src/fastapi_app

COPY ../requirements.txt .

RUN pip3 install --no-cache-dir -r app/requirements.txt

COPY .. ./app

# Ignore UserWarning (mobile_sam package)
ENV PYTHONWARNINGS=ignore