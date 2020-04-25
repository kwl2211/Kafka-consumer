
FROM golang:1.9 

RUN go get github.com/Shopify/sarama
RUN go get github.com/wvanbergen/kafka/consumergroup
RUN go get github.com/prometheus/client_golang/prometheus/promhttp

# ENV ZOOKEEPER_HOST localhost
# ENV ZOOKEEPER_PORT 2181
# ENV TOPIC senz

RUN mkdir /app
ADD . /app
WORKDIR /app
RUN go build -o main .
CMD ["/app/main"]
