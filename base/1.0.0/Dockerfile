FROM ubuntu:20.10
LABEL author="Gervaise H. Henry"

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update -y --fix-missing && apt-get upgrade -y
RUN apt-get install -y gcc g++ apt-utils wget gzip pigz pbzip2 zip software-properties-common make parallel pandoc git curl