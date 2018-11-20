FROM centos:centos7
MAINTAINER fufu

#install nginx
RUN yum -y --setopt=tsflags=nodocs update && \
    yum -y --setopt=tsflags=nodocs install epel-release && \
    yum -y --setopt=tsflags=nodocs install nginx && \
    yum clean all

#add nginx.conf file to images
ADD nginx.conf /etc/nginx/nginx.conf

# chown of folder the user nginx used
RUN chmod -R go+rwx /var/log/nginx

RUN chmod -R go+rwx /var/lib/nginx

# expose container port 8080
EXPOSE 8080

# switch to user nginx
USER nginx

ENTRYPOINT [ "/usr/sbin/nginx" ]
