FROM jboss/base-jdk:7


# Add EAP_HOME environment variable, to easily upgrade the script for different EAP versions


# Add default admin user
RUN ${EAP_HOME}/bin/add-user.sh admin admin123! --silent

# Enable binding to all network interfaces and debugging inside the EAP
RUN echo "JAVA_OPTS=\"\$JAVA_OPTS -Djboss.bind.address=0.0.0.0 -Djboss.bind.address.management=0.0.0.0\"" >> ${EAP_HOME}/bin/standalone.conf

# Add volume if you want to externalize logs
VOLUME ${EAP_HOME}/standalone/logs




CMD []