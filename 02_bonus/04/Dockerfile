FROM ubuntu

ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get upgrade -y && apt-get install -y python3.6 vim git lldb

ENTRYPOINT lldb
