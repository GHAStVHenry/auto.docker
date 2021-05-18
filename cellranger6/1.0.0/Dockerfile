FROM ghhenry/base:1.0.0
LABEL author="Gervaise H. Henry"

RUN apt-get install -y unzip alien && \
  wget 'https://files.softwaredownloads.illumina.com/e8ed3335-5201-48ff-a2bc-db4bfb792c85/bcl2fastq2-v2-20-0-linux-x86-64.zip?Expires=1621307165&Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9maWxlcy5zb2Z0d2FyZWRvd25sb2Fkcy5pbGx1bWluYS5jb20vZThlZDMzMzUtNTIwMS00OGZmLWEyYmMtZGI0YmZiNzkyYzg1L2JjbDJmYXN0cTItdjItMjAtMC1saW51eC14ODYtNjQuemlwIiwiQ29uZGl0aW9uIjp7IkRhdGVMZXNzVGhhbiI6eyJBV1M6RXBvY2hUaW1lIjoxNjIxMzA3MTY1fX19XX0_&Signature=JVryZXdgQa5gxHXzCKxejOrRD7i0IYHmGTniEEl4aNquhZoiP7VcWQoi8gltJoqZNwQlFaFdnxayqMj5wzhy8R2mx89Dy0Z2JcswTwZ~hohNB~l97kYgzxJH-S8O~OFaMxiTgxlU5UM6EbJQiw~lJh28Ry84BrYF~00ZaK92gql1Ut9xWv3tqX~wSywEt84AxzsPaGVFYvdPN0Rd2lkt6pxttHRAj-Q955PfB8iEmvrbvm9lYhsDlL20kentnK2S54yFoV2e-9HoTuCSqF-7OEr0DpGRTF~fSFhCfi0OMk4JYPJ3L6dwSVcQhi4E2CK-YpjyGm~-IID2P1iSDXX5tQ__&Key-Pair-Id=APKAJO3UYWPXK4A26FPQ' -O bcl2fastq2-v2-20-0-linux-x86-64.zip && \
  unzip bcl2fastq2-v2-20-0-linux-x86-64.zip && \
  alien -i bcl2fastq2-v2.20.0.422-Linux-x86_64.rpm && \
  rm  bcl2fastq2*

RUN cd /opt && \
  wget -O cellranger-6.0.1.tar.gz "https://cf.10xgenomics.com/releases/cell-exp/cellranger-6.0.1.tar.gz?Expires=1621350089&Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9jZi4xMHhnZW5vbWljcy5jb20vcmVsZWFzZXMvY2VsbC1leHAvY2VsbHJhbmdlci02LjAuMS50YXIuZ3oiLCJDb25kaXRpb24iOnsiRGF0ZUxlc3NUaGFuIjp7IkFXUzpFcG9jaFRpbWUiOjE2MjEzNTAwODl9fX1dfQ__&Signature=awV~Uy7erZHYDZAk8RGO5~Uf4f5W6E3Jz8fkK4AMYm~WgnwzK2cUpcc0SLeV0N5jq5BeWfGd9jFIMgUnwHBCN2sW4B5GYv7mupmwN4xsCsufgnW1Qt5WYUny3X8OELcIGT0aAlsa2Stsbfn6jbIYAiOmSX8uNUn0EUUrkj~ZH6KfKUqlWPQcg6Tab~XyACex0fESj8f3J7Ezz2gwruTHusqzMdfQcd3TivHNsPp~UAQ~utYhesDiGxoX4RYGUDYUADVnzE0uh254AHRWkgeu028QvTTNswi8ma3M56fKiAdFI5OGu5m8rtxdd6WjxkJphRS21MbJrGpi~TCKZpuR1w__&Key-Pair-Id=APKAI7S6A5RYOXBWRPDA" && \
  tar -xzvf cellranger-6.0.1.tar.gz
ENV PATH=/opt/cellranger-6.0.1:$PATH