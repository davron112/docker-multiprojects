 ถ้า call หากันไม่ได้ ให้ใช้  ip ของ nginx https://github.com/laradock/laradock/issues/435


      ports:
        - "${APACHE_HOST_HTTP_PORT}:80"
        - "${APACHE_HOST_HTTPS_PORT}:443"
 