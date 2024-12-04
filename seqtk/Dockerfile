# Usa un'immagine base leggera con gli strumenti necessari
FROM ubuntu:24.10

# Aggiorna il sistema e installa dipendenze necessarie
RUN apt-get update && apt-get install -y \
    build-essential \
    zlib1g-dev \
    git \
    && apt-get clean

# Clona il repository, entra nella directory e compila seqtk
RUN git clone https://github.com/lh3/seqtk.git && \
    cd seqtk && \
    make && \
    mv seqtk /bin

USER root
