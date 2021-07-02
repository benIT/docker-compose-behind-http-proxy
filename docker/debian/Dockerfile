FROM debian:stretch
RUN rm -rf /var/lib/apt/lists/*
RUN apt-get update
RUN apt-get install -y curl
COPY *.crt /usr/local/share/ca-certificates/
RUN update-ca-certificates
RUN echo "################################testing a curl HTTP request###########################################"
RUN curl -s http://example.com/ > /dev/null
RUN echo "################################testing a curl HTTPS request###########################################"
RUN curl -s https://example.com/ > /dev/null