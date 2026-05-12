FROM ubuntu:22.04

COPY workspace/setup.sh /setup.sh
RUN chmod +x /setup.sh && /setup.sh

WORKDIR /app

CMD ["/bin/bash"]
