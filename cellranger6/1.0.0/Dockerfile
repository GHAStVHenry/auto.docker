FROM ghhenry/base:1.0.0
LABEL author="Gervaise H. Henry"

RUN apt-get install -y alien unzip && \
  wget https://files.softwaredownloads.illumina.com/e8ed3335-5201-48ff-a2bc-db4bfb792c85/bcl2fastq2-v2-20-0-linux-x86-64.zip?Expires=1621053739&Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9maWxlcy5zb2Z0d2FyZWRvd25sb2Fkcy5pbGx1bWluYS5jb20vZThlZDMzMzUtNTIwMS00OGZmLWEyYmMtZGI0YmZiNzkyYzg1L2JjbDJmYXN0cTItdjItMjAtMC1saW51eC14ODYtNjQuemlwIiwiQ29uZGl0aW9uIjp7IkRhdGVMZXNzVGhhbiI6eyJBV1M6RXBvY2hUaW1lIjoxNjIxMDUzNzM5fX19XX0_&Signature=kT-zLauTnCOz~2mzhj1rcYzpX25lcM9ELsfd-exNembmi-66a0IkWo2sUEiY6v5RtzUP~gTfKzSNr9fOSgjXkxHpwNj-QTbnQhNagGlt2qwa1VCjfbkxM7a1S9-ciHOROLrM4MNe0jfAjr4RMFSgBjdl7Pj4SWif-Ho4JgIXOZ1p1bFwMx~17icJoD7CeNtNhyyxT5ryn-P1NFNeA5djXF~n8H0NfZTjC9HnVOSan~Ohfqum6gn22zyso-bWgw1EKX9bQ8q5KcLMNXT~LltD5FndnGsU9Ni1BwlsHpDwhRcsnXwDb7khrGd47v0b8ovvJb-40EfLFwHAunVV2CFR3g__&Key-Pair-Id=APKAJO3UYWPXK4A26FPQ && \
  unzip bcl2fastq*.zip && \
  alien -i bcl2fastq*.rpm && \
  rm bcl2fastq*.rpm

RUN cd /opt && \
  wget -O cellranger-6.0.1.tar.gz "https://cf.10xgenomics.com/releases/cell-exp/cellranger-6.0.1.tar.gz?Expires=1621093510&Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9jZi4xMHhnZW5vbWljcy5jb20vcmVsZWFzZXMvY2VsbC1leHAvY2VsbHJhbmdlci02LjAuMS50YXIuZ3oiLCJDb25kaXRpb24iOnsiRGF0ZUxlc3NUaGFuIjp7IkFXUzpFcG9jaFRpbWUiOjE2MjEwOTM1MTB9fX1dfQ__&Signature=funnk9sCxzNcqgJpHUIz1855NrUQXHlfWZ6kFXvukPDiv2ffM0rd4IseXq05T7LQEDsOVvkxUIdqP2ov40ri5FfX8xyZhz52TVRvWzToCA0zxtDnMXQTzAgDrqlmmthhFPH0Jc3p38jn3sLwPUqjmIDjnoTmXjDPhLSOzgY66TH~LJv9Xn1uJ31NhtcsFs4-FPCFakKCoVSJkDWp57GCj5~lmVLBE5BXxPv~eOt1Zn6F~Dn4HWLqRXYoyc8AMp-cRLmr7zt-YzKTAMDSuTBVELzsYe3lGA1ffvCnZ3fzEokF3gp3hIypdCtRL4h3AM0AKaXH5mP-BfnYP5V2fBX0jg__&Key-Pair-Id=APKAI7S6A5RYOXBWRPDA" && \
  tar -xzvf cellranger-6.0.1.tar.gz
ENV PATH=/opt/cellranger-6.0.1:$PATH