FROM dustynv/opencv:4.8.1-r36.2.0

WORKDIR /usr/src/fastapi_app

RUN pip install https://nvidia.box.com/shared/static/mp164asf3sceb570wvjsrezk1p4ftj8t.whl
RUN pip install https://nvidia.box.com/shared/static/xpr06qe6ql3l6rj22cu3c45tz1wzi36p.whl


COPY ../requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt

COPY .. ./app

# Ignore UserWarning (mobile_sam package)
ENV PYTHONWARNINGS=ignore

EXPOSE 8000
