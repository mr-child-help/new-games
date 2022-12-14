---
title: Git Large File Storage herabstufen
intro: 'Sie können Speicher und Bandbreite für {% data variables.large_files.product_name_short %} in Stufen von je 50 GB pro Monat herabstufen.'
redirect_from:
  - /github/setting-up-and-managing-billing-and-payments-on-github/downgrading-git-large-file-storage
  - /articles/downgrading-storage-and-bandwidth-for-a-personal-account/
  - /articles/downgrading-storage-and-bandwidth-for-an-organization/
  - /articles/downgrading-git-large-file-storage
  - /github/setting-up-and-managing-billing-and-payments-on-github/managing-billing-for-git-large-file-storage/downgrading-git-large-file-storage
versions:
  fpt: '*'
  ghec: '*'
type: how_to
topics:
  - Downgrades
  - LFS
  - Organizations
  - User account
shortTitle: Downgrade Git LFS storage
---

Wenn Du die Anzahl Deiner Datenpakete herabstufst, werden Deine Änderungen zum nächsten Abrechnungsdatum wirksam. Weitere Informationen findest Du unter „[Informationen zur Abrechnung für {% data variables.large_files.product_name_long %}](/articles/about-billing-for-git-large-file-storage).“

## Speicher und Bandbreite für ein persönliches Konto herabstufen

{% data reusables.user_settings.access_settings %}
{% data reusables.user_settings.billing_plans %}
{% data reusables.dotcom_billing.lfs-remove-data %}
{% data reusables.large_files.downgrade_data_packs %}

## Speicher und Bandbreite für eine Organisation herabstufen

{% data reusables.dotcom_billing.org-billing-perms %}

{% data reusables.organizations.billing-settings %}
{% data reusables.dotcom_billing.lfs-remove-data %}
{% data reusables.large_files.downgrade_data_packs %}
