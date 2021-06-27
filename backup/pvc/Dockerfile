FROM debian:buster-slim

ARG UID="1000"
ARG GID="1000"

ENV USER=user

RUN addgroup --gid "$GID" "$USER" && \
    adduser \
    --disabled-password \
    --gecos "" \
    --ingroup "$USER" \
    --uid "$UID" \
    "$USER"

WORKDIR /home/user/bin
COPY bin .
RUN chmod +x *.sh
USER user

CMD ./run.sh
