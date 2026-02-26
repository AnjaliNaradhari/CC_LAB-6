FROM ubuntu:20.04

RUN apt update && apt install -y g++

WORKDIR /app

COPY app.cpp .

RUN g++ app.cpp -o app

CMD ["./app"]
