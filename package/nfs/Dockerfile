FROM debian:stretch
RUN apt-get update && \
    apt-get install -y jq curl nfs-common procps
COPY storage /usr/bin/
COPY nfs/rancher-nfs common/* /usr/bin/
CMD ["start.sh", "storage", "--driver-name", "rancher-nfs"]
