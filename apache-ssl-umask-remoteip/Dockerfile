FROM 459below/nextcloud-armv7:ssl

COPY docker-entrypoint.sh /entrypoint.sh
COPY remoteip.conf /etc/apache2/conf-available/remoteip.conf

RUN [ "cross-build-start" ]

RUN a2enmod remoteip \
 && a2enconf remoteip

RUN [ "cross-build-end" ]

ENTRYPOINT ["/entrypoint.sh"]
CMD ["apache2-foreground"]
