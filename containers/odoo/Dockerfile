FROM quay.io/acsone/odoo-bedrock:12.0-py36-latest

RUN set -e \
  && apt update \
  && apt -y install --no-install-recommends postgresql-client \
  && apt -y clean \
  && rm -rf /var/lib/apt/lists/*

COPY ./entrypoint-db /odoo/start-entrypoint.d/

COPY ./requirements.txt /tmp/

RUN pip install -r /tmp/requirements.txt

