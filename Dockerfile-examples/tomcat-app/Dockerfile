####Steps to build tomcat-app

# Pull centos from dockerhub                                        FROM
# Install java                                                      RUN
# Create /opt/tomcat directory                                      RUN
# Changes work directory to /opt/tomcat                             WORKDIR 
# Download tomcat packages                                          ADD<tomcat URL>/RUN
# Extract tar.gz                                                    RUN
# Rename to tomcat directory                                        RUN
# Tell to docker that it runs on port 8080                          EXPOSE
# Start tomcat services                                             CMD 

FROM centos:latest
RUN sed -i 's/mirrorlist/#mirrorlist/g' /etc/yum.repos.d/CentOS-*
RUN sed -i 's|#baseurl=http://mirror.centos.org|baseurl=http://vault.centos.org|g' /etc/yum.repos.d/CentOS-*
RUN yum install java -y
RUN mkdir /opt/tomcat
WORKDIR /opt/tomcat
ADD https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.70/bin/apache-tomcat-9.0.70.tar.gz .
RUN tar -xvzf apache-tomcat-9.0.70.tar.gz 
RUN mv apache-tomcat-9.0.70/* /opt/tomcat/
EXPOSE 8080
CMD ["/opt/tomcat/bin/catalina.sh", "run"]
