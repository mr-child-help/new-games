---
title: Verifizierungsstatus der Commit- und Tag-Signaturen prüfen
intro: 'Sie können den Verifizierungsstatus Ihrer Commit- und Tag-Signaturen auf {% data variables.product.product_name %} überprüfen.'
redirect_from:
  - /articles/checking-your-gpg-commit-and-tag-signature-verification-status/
  - /articles/checking-your-commit-and-tag-signature-verification-status
  - /github/authenticating-to-github/checking-your-commit-and-tag-signature-verification-status
  - /github/authenticating-to-github/troubleshooting-commit-signature-verification/checking-your-commit-and-tag-signature-verification-status
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Identity
  - Access management
shortTitle: Check verification status
---

## Den Verifizierungsstatus Deiner Commit-Signatur prüfen

1. Navigieren Sie auf {% data variables.product.product_name %} zu Ihrem Pull Request.
{% data reusables.repositories.review-pr-commits %}
3. Next to your commit's abbreviated commit hash, there is a box that shows whether your commit signature is verified{% ifversion fpt or ghec %}, partially verified,{% endif %} or unverified. ![Signierter Commit](/assets/images/help/commits/gpg-signed-commit-verified-without-details.png)
4. To view more detailed information about the commit signature, click **Verified**{% ifversion fpt or ghec %}, **Partially verified**,{% endif %} or **Unverified**. ![Verifizierter signierter Commit](/assets/images/help/commits/gpg-signed-commit_verified_details.png)

## Den Verifizierungsstatus Deiner Tag-Signatur überprüfen

{% data reusables.repositories.navigate-to-repo %}
{% data reusables.repositories.releases %}
2. Klicke oben auf der Releases-Seite auf **Tags**. ![Tags-Seite](/assets/images/help/releases/tags-list.png)
3. Next to your tag description, there is a box that shows whether your tag signature is verified{% ifversion fpt or ghec %}, partially verified,{% endif %} or unverified. ![Verifizierte Tag-Signatur](/assets/images/help/commits/gpg-signed-tag-verified.png)
4. To view more detailed information about the tag signature, click **Verified**{% ifversion fpt or ghec %}, **Partially verified**,{% endif %} or **Unverified**. ![Verifizierter signierter Tag](/assets/images/help/commits/gpg-signed-tag-verified-details.png)

## Weiterführende Informationen

- „[Informationen zur Verifizierung einer Commit-Signatur](/articles/about-commit-signature-verification)“
- „[Commits signieren](/articles/signing-commits)“
- „[Tags signieren](/articles/signing-tags)“
