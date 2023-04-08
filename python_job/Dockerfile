FROM python:3.9.15-alpine3.16

ARG UID=1000
ARG GID=1001
RUN addgroup -g $GID pyuser && adduser --home /app --disabled-password -u $UID -guid $GID pyuser
USER $UID

WORKDIR /app
COPY --chown=$UID:$GID . .

ENTRYPOINT ["python", "main.py"]
