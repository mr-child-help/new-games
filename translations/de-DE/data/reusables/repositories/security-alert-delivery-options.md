{% ifversion not ghae %}
If your repository has a supported dependency manifest
{% ifversion fpt or ghec %} (and if you've set up the dependency graph if it's a private repository){% endif %}, whenever {% data variables.product.product_name %} detects a vulnerable dependency in your repository, you will receive a weekly digest email. Darüber hinaus können Sie Ihre Sicherheitsmeldungen als Webbenachrichtigungen, einzelne E-Mail-Benachrichtigungen, tägliche E-Mail-Digests oder Meldungen auf der {% data variables.product.product_name %}-Oberfläche konfigurieren. For more information, see "[About alerts for vulnerable dependencies](/github/managing-security-vulnerabilities/about-alerts-for-vulnerable-dependencies)." |
{% endif %}
