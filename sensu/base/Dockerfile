FROM registry.access.redhat.com/rhel7/rhel
MAINTAINER Michael Zamot mzamot@redhat.com

# Add Sensu repository
ADD files/sensu.repo /etc/yum.repos.d/

RUN yum repolist --disablerepo=* && \
    yum-config-manager --disable \* > /dev/null && \
    yum-config-manager --enable rhel-7-server-rpms > /dev/null && \ 
    yum-config-manager --enable sensu && \
    yum install -y sensu && \
    yum clean all && \
    rm -rf /etc/sensu/config.json.example 

ADD conf.d /etc/sensu/conf.d/
