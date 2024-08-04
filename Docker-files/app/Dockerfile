FROM openjdk:11 AS BUILD_IMAGE
LABEL PROJECT="VProfile"
LABEL AUTHOR="AnNgo"

RUN apt update && apt install maven -y
RUN git clone -b docker https://github.com/DuyAn1999/vprofile-project.git
RUN cd vprofile-project && mvn install

FROM tomcat:9-jre11
LABEL PROJECT="VProfile"
LABEL AUTHOR="AnNgo"
RUN rm -rf /usr/local/tomcat/webapps/*
COPY --from=BUILD_IMAGE vprofile-project/target/vprofile-v2.war /usr/local/tomcat/webapps/ROOT.war
EXPOSE 8080
CMD ["catalina.sh", "run"]
WORKDIR /usr/local/tomcat/
VOLUME /usr/local/tomcat/webapps