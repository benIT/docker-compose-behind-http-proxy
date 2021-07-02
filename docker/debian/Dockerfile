FROM debian:stretch
RUN echo "http_proxy: $http_proxy | https_proxy: $https_proxy | no_proxy: $no_proxy"
RUN rm -rf /var/lib/apt/lists/*
RUN apt-get update
RUN apt-get install -y curl
COPY *.crt /usr/local/share/ca-certificates/
RUN update-ca-certificates
RUN echo "################################testing a curl HTTP request###########################################"
RUN curl -s http://example.com/ > /dev/null
RUN echo "################################testing a curl HTTPS request###########################################"
RUN curl https://example.com/ > /dev/null