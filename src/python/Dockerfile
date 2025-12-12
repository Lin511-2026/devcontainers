# ARG BASE_IMAGE=python
# ARG QUARTOVERSION=1.5.56
# ARG VARIANT=3.13-bookworm
# FROM ${BASE_IMAGE}:${VARIANT}
FROM python:3.13-bookworm
COPY --from=ghcr.io/astral-sh/uv:latest /uv /uvx /bin/

# install requirements
COPY ./uv.lock .
RUN uv sync

# # # quarto update
# ARG QUARTOVERSION
# RUN cd /usr/share/ \
#     && wget https://github.com/quarto-dev/quarto-cli/releases/download/v${QUARTOVERSION}/quarto-${QUARTOVERSION}-linux-amd64.tar.gz \
#     && tar -xvzf quarto-${QUARTOVERSION}-linux-amd64.tar.gz && mv quarto-${QUARTOVERSION} .quarto \
#     && rm /usr/local/bin/quarto \
#     && ln -s .quarto quarto

# ENV PATH "$PATH:/usr/share/quarto/bin"
