FROM centos:latest
ENV SS_PASS=SHADOWSOCKS_PASSWORD
#RUN yum update -y
#RUN yum install -y util-linux-user
WORKDIR /usr/local/bin
COPY go-shadowsocks2 .
COPY v2ray-plugin .
COPY ssv2ray .
RUN chmod +x go-shadowsocks2
RUN chmod +x v2ray-plugin
RUN chmod +x ssv2ray
CMD ["/bin/bash", "-c", "ssv2ray"]
