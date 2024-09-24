# Custom image for nextcloud's cron. It adds a cron entry to crontabs which generates images' previews every 5 minutes.

FROM nextcloud

RUN echo '*/5 * * * * php /var/www/html/occ preview:pre-generate' >> /var/spool/cron/crontabs/www-data

ENTRYPOINT ["/cron.sh"]
