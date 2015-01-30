## Use the official docker centos distribution ##
FROM brianbland/ldap-base:latest

## Get some karma ##
MAINTAINER Brian Bland, brian.bland@docker.com

COPY . /root

# Default password is Welcome0 
RUN service slapd start && sleep 3 && ldapadd -f /root/ldap2.ldif -D cn=Manager,dc=example,dc=com -w welcome0

EXPOSE 389

VOLUME [ "/data" ]

CMD ["/root/run.sh"]
