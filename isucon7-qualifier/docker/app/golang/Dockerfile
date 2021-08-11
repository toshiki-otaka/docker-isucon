FROM golang:1.9

ARG GIT_URL=https://github.com/toshiki-otaka/isucon7-qualify.git

RUN git clone $GIT_URL /home/isucon/isubata
RUN go get -u github.com/golang/dep/cmd/dep
RUN dep ensure
WORKDIR /home/isucon/isubata/webapp/go
RUN make

EXPOSE 5000

ENTRYPOINT ["/home/isucon/isubata/webapp/go/isubata"]
