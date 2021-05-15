FROM ghhenry/base:1.0.0
LABEL author="Gervaise H. Henry"

RUN cd /opt && \
  wget -O cellranger-6.0.1.tar.gz "https://cf.10xgenomics.com/releases/cell-exp/cellranger-6.0.1.tar.gz?Expires=1621093510&Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9jZi4xMHhnZW5vbWljcy5jb20vcmVsZWFzZXMvY2VsbC1leHAvY2VsbHJhbmdlci02LjAuMS50YXIuZ3oiLCJDb25kaXRpb24iOnsiRGF0ZUxlc3NUaGFuIjp7IkFXUzpFcG9jaFRpbWUiOjE2MjEwOTM1MTB9fX1dfQ__&Signature=funnk9sCxzNcqgJpHUIz1855NrUQXHlfWZ6kFXvukPDiv2ffM0rd4IseXq05T7LQEDsOVvkxUIdqP2ov40ri5FfX8xyZhz52TVRvWzToCA0zxtDnMXQTzAgDrqlmmthhFPH0Jc3p38jn3sLwPUqjmIDjnoTmXjDPhLSOzgY66TH~LJv9Xn1uJ31NhtcsFs4-FPCFakKCoVSJkDWp57GCj5~lmVLBE5BXxPv~eOt1Zn6F~Dn4HWLqRXYoyc8AMp-cRLmr7zt-YzKTAMDSuTBVELzsYe3lGA1ffvCnZ3fzEokF3gp3hIypdCtRL4h3AM0AKaXH5mP-BfnYP5V2fBX0jg__&Key-Pair-Id=APKAI7S6A5RYOXBWRPDA" && \
  tar -xzvf cellranger-6.0.1.tar.gz
ENV PATH=/opt/cellranger-6.0.1:$PATH