FROM ghhenry/base:1.0.0
LABEL author="Gervaise H. Henry"

RUN apt-get install -y unzip alien && \
  wget 'https://fileshttps://files.softwaredownloads.illumina.com/e8ed3335-5201-48ff-a2bc-db4bfb792c85/bcl2fastq2-v2-20-0-linux-x86-64.zip?Expires=1621308567&Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9maWxlcy5zb2Z0d2FyZWRvd25sb2Fkcy5pbGx1bWluYS5jb20vZThlZDMzMzUtNTIwMS00OGZmLWEyYmMtZGI0YmZiNzkyYzg1L2JjbDJmYXN0cTItdjItMjAtMC1saW51eC14ODYtNjQuemlwIiwiQ29uZGl0aW9uIjp7IkRhdGVMZXNzVGhhbiI6eyJBV1M6RXBvY2hUaW1lIjoxNjIxMzA4NTY3fX19XX0_&Signature=UckeF39c8PT3QoMhc8cvP5ley0KF29LIqgoRNza-x6S53ryYs2TH8bcU6pZ5jQDEaxRFM0MZBNJmMXjixDGQfgAxivayPK2AIpk0nicJGsuMQzAI9uWGuJrh-yxmcnePIxLAcVa16MeRMk2nyzQusTn3Mhdf125tGp8dJC5jc3PUqADXDMKi8va766mT2MoL6NjMq4zDa8EiOTqqWfd1CFlIQPskLyE6SU4~WCnKERdyZrmuasf-LIXq2HdCAyLlzbHw--FEeO6SqfhFC4H3foAR8AExp3Lx2Wr2Joz0MY6WNodz1yP5jUg-JIRINGQo5ZhDE8saetvtrivgcP5bxQ__&Key-Pair-Id=APKAJO3UYWPXK4A26FPQ' -O bcl2fastq2-v2-20-0-linux-x86-64.zip && \
  unzip bcl2fastq2-v2-20-0-linux-x86-64.zip && \
  alien -i bcl2fastq2-v2.20.0.422-Linux-x86_64.rpm && \
  rm  bcl2fastq2*

RUN cd /opt && \
  curl -o cellranger-5.0.1.tar.gz "https://cf.10xgenomics.com/releases/cell-exp/cellranger-5.0.1.tar.gz?Expires=1621351486&Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9jZi4xMHhnZW5vbWljcy5jb20vcmVsZWFzZXMvY2VsbC1leHAvY2VsbHJhbmdlci01LjAuMS50YXIuZ3oiLCJDb25kaXRpb24iOnsiRGF0ZUxlc3NUaGFuIjp7IkFXUzpFcG9jaFRpbWUiOjE2MjEzNTE0ODZ9fX1dfQ__&Signature=JCGZN-~grt208duOGaeM8szAVTFU5Ayctq8TiYqnODiww4ERJqn0ePxf8rmIEQDXTRe6X6R-n6VlpZtVhVIMfo9z4ppg~4qPxTCFejeTAUahzOCfrOKHqTuOj~8kA7tsL~EZqbEF9pOOBQl7Ycwsp5kaOiLd03J5SBlJubqdDRXJrrljKxk1qNmgYJTgE~AJ-KuREUf~-bwb~pUkFUqdBcC0w2gk82ZXjGF31omDU7dnABZNfDCgUsXHl5qqCTKTbLmvH1-qeXXQl83VNNeI8h8D3ATDY7hUPqnFgeX7Vr5sfYd3xtftJ1Rrcs~uh5bQJVCTT8XvI0HQsPKfinysAA__&Key-Pair-Id=APKAI7S6A5RYOXBWRPDA" && \
  tar -xzvf cellranger-5.0.1.tar.gz
ENV PATH=/opt/cellranger-5.0.1:$PATH