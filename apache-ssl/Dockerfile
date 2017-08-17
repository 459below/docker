FROM 459below/nextcloud-armv7

RUN [ "cross-build-start" ]

RUN a2enmod ssl \
 && a2ensite default-ssl

RUN [ "cross-build-end" ]

EXPOSE 443

ENTRYPOINT ["/entrypoint.sh"]
CMD ["apache2-foreground"]
