FROM tamuhey/juman:py3.7.6-1.0.2

ENV KNP_VERSION 4.19
ENV KNP_URL "http://nlp.ist.i.kyoto-u.ac.jp/DLcounter/lime.cgi?down=http://nlp.ist.i.kyoto-u.ac.jp/nl-resource/knp/knp-${KNP_VERSION}.tar.bz2&name=knp-${KNP_VERSION}.tar.bz2"

RUN cd /tmp && \
    wget ${KNP_URL} -O knp.tar.bz2 && tar jxvf knp.tar.bz2 && cd knp-${KNP_VERSION} && ./configure && make && make install && \
    rm -rf /tmp/*
