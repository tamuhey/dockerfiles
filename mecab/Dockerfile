FROM python:3.7.6

ENV MECAB_URL "https://drive.google.com/uc?export=download&id=0B4y35FiV1wh7cENtOXlicTFaRUE"
ENV IPADIC_URL "https://drive.google.com/uc?export=download&id=0B4y35FiV1wh7MWVlSDBCSXZMTXM"

# install mecab
RUN cd /tmp && \
    wget --no-check-certificate ${MECAB_URL} -O mecab.tar.gz && \
    tar xzvf mecab.tar.gz && cd mecab-0.996 && ./configure && make && make check && make install && \
    rm -rf /tmp/*
# install ipadic
RUN cd /tmp && \
    wget --no-check-certificate ${IPADIC_URL} -O ipadic.tar.gz && \
    tar xzvf ipadic.tar.gz && cd mecab-ipadic-2.7.0-20070801 && ./configure --with-charset=utf8 && ldconfig && make && make install && \
    rm -rf /tmp/*

