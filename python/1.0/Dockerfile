# Dockerfile to MAC Address Manufacturer Lookup container.

# Official Dockerfile used: https://hub.docker.com/_/python
FROM python:2.7

MAINTAINER Roger CARHUATOCTO <chilcano at intix dot info>

RUN pip install unicodecsv
RUN pip install Flask
RUN pip install sqlalchemy

# Allocate the 5000 to run a HTTP server
EXPOSE 5000

COPY mac_manuf_wireshark_file.py /
COPY mac_manuf_table_def.py /
COPY mac_manuf_api_rest.py /

RUN python mac_manuf_wireshark_file.py
CMD python mac_manuf_api_rest.py
