FROM sdnm/cassini-odtn:latest

WORKDIR /root

COPY init-service.sh .

LABEL br.rnp.label.name="cassini-sdnm"\
      br.rnp.label.description="SDN transponder cassini from ODTN with dataplane by RNP"\
      br.rnp.label.vendor="National Network for Education and Research - RNP"\
      br.rnp.label.contact="fernando.farias@rnp.br"\
      br.rnp.label.application="CNetLab"\
      br.rnp.label.version="0.1"\
      br.rnp.label.license="Apache2"

RUN git clone https://github.com/fernnf/cassini-dataplane.git

ENV PYTHONPATH /root/cassini-dataplane/

RUN chmod +x /root/init-service.sh

CMD ["/root/init-service.sh"]