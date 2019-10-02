#############################################################################
FROM oneartifactory.verizon.com:8091/vzw/b6vv/orbpm/orbpm-centosopenjdk-baseimg:v1.0

ARG jar_name=poc_config
ARG version=1.0.0
ARG packaging_type=jar


####### MAINTAINER ############
MAINTAINER "Saran Teja, Patnala" "v.n.v.saran.patnala@verizon.com"

########################CREATE FOLDER STRUCTURE############################
RUN mkdir -p /app/application/logs/

# Add application jar
ADD poc_config.jar /app/application/poc_config.jar

RUN chmod 775 /app/application/poc_config.jar

RUN sh -c 'touch /app/application/poc_config.jar'

EXPOSE 8123



ENTRYPOINT ["java","-jar","/app/application/poc_config.jar"]