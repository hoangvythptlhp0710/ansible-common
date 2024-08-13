// chưa hỗ trợ cấu hình version nginx

{{ 'ssl_certificate'    + item.ssl_certificate_path | default('default_ssl_certificate_path') + item.certificate_name + ';' if item.certificate_name is defined}}
{{ 'ssl_certificate_key'    + item.ssl_certificate_path | default('default_ssl_certificate_path') + item.certificate_key + ';' if item.certificate_key is defined}}

    {{ 'ssl_session_timeout'    + item.ssl_session_timeout | default('default_ssl_session_timeout') + ';' if item.ssl_session_timeout is defined}}
    {{ 'ssl_protocols'    + item.ssl_protocols | default('default_ssl_protocols') + ';' if item.ssl_protocols is defined}}
    {{ 'ssl_ciphers'    + item.ssl_ciphers | default('default_ssl_ciphers') + ';' if item.ssl_ciphers is defined}}
    {{ 'ssl_prefer_server_ciphers'    + item.ssl_prefer_server_ciphers | default('default_ssl_prefer_server_ciphers') + ';' if item.ssl_prefer_server_ciphers is defined}}
