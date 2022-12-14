---
title: About billing for GitHub Advanced Security
intro: 'If you want to use {% data variables.product.prodname_GH_advanced_security %} features{% ifversion fpt or ghec %} in a private or internal repository{% endif %}, you need a license.{% ifversion fpt or ghec %} These features are available free of charge for public repositories on {% data variables.product.prodname_dotcom_the_website %}.{% endif %}'
product: '{% data reusables.gated-features.ghas %}'
redirect_from:
  - /admin/advanced-security/about-licensing-for-github-advanced-security
  - /billing/managing-licensing-for-github-advanced-security/about-licensing-for-github-advanced-security
  - /github/setting-up-and-managing-billing-and-payments-on-github/about-licensing-for-github-advanced-security
  - /github/setting-up-and-managing-billing-and-payments-on-github/managing-licensing-for-github-advanced-security/about-licensing-for-github-advanced-security
versions:
  fpt: '*'
  ghes: '>=3.1'
  ghec: '*'
type: overview
topics:
  - Advanced Security
  - Enterprise
  - Licensing
shortTitle: Advanced Security billing
---

## About billing for {% data variables.product.prodname_GH_advanced_security %}

{% ifversion fpt or ghec %}

If you want to use {% data variables.product.prodname_GH_advanced_security %} features on any repository apart from a public repository on {% data variables.product.prodname_dotcom_the_website %}, you will need a license. For more information about {% data variables.product.prodname_GH_advanced_security %}, see "[About {% data variables.product.prodname_GH_advanced_security %}](/github/getting-started-with-github/about-github-advanced-security)."

{% elsif ghes %}

You can make extra features for code security available to users by buying and uploading a license for {% data variables.product.prodname_GH_advanced_security %}. For more information about {% data variables.product.prodname_GH_advanced_security %}, see "[About {% data variables.product.prodname_GH_advanced_security %}](/github/getting-started-with-github/about-github-advanced-security)."

{% endif %}

{% ifversion fpt or ghes or ghec %}

{% data reusables.advanced-security.license-overview %}

{% endif %}

To discuss licensing {% data variables.product.prodname_GH_advanced_security %} for your enterprise, contact {% data variables.contact.contact_enterprise_sales %}.

## About committer numbers for {% data variables.product.prodname_GH_advanced_security %}

{% data reusables.advanced-security.about-committer-numbers-ghec-ghes %}

{% ifversion fpt or ghes or ghec %}

{% data reusables.advanced-security.managing-license-usage-ghec-ghes %}

{% endif %}

You can enforce policies to allow or disallow the use of {% data variables.product.prodname_advanced_security %} by organizations owned by your enterprise account. For more information, see "[Enforcing policies for {% data variables.product.prodname_advanced_security %} in your enterprise]({% ifversion fpt %}/enterprise-cloud@latest/{% endif %}/admin/policies/enforcing-policies-for-your-enterprise/enforcing-policies-for-advanced-security-in-your-enterprise){% ifversion fpt %}" in the {% data variables.product.prodname_ghe_cloud %} documentation.{% else %}."{% endif %}

{% ifversion fpt or ghes or ghec %}

For more information on viewing license usage, see "[Viewing your {% data variables.product.prodname_GH_advanced_security %} usage](/billing/managing-billing-for-github-advanced-security/viewing-your-github-advanced-security-usage)."

{% endif %}

## Calculating committer spending

The following example timeline demonstrates the events during a month that affect billing for {% data variables.product.prodname_GH_advanced_security %} in an enterprise. For each month, you will find events, the total committer count, and the total number of committers that {% data variables.product.company_short %} would bill for.

<table spaces-before="0">
  <tr>
    <th align="left">
      Date
    </th>
    
    <th align="left">
      Events during the month
    </th>
    
    <th align="right">
      Total committer count
    </th>
    
    <th align="right">
      Committers billed for the month
    </th>
  </tr>
  
  <tr>
    <td align="left">
      <nobr>August 1</nobr>
    </td>
    
    <td align="left">
      A member of your enterprise enables {% data variables.product.prodname_GH_advanced_security %} for repository <strong x-id="1">X</strong>. Repository <strong x-id="1">X</strong> has 50 committers over the past 90 days.
    </td>
    
    <td align="right">
      <strong x-id="1">50</strong>
    </td>
    
    <td align="right">
      <strong x-id="1">50</strong>
    </td>
  </tr>
  
  <tr>
    <td align="left">
      <nobr>September 5</nobr>
    </td>
    
    <td align="left">
      Developer <strong x-id="1">A</strong> leaves the team working on repository <strong x-id="1">X</strong>. Developer <strong x-id="1">A</strong>'s contributions continue to count for 90 days.
    </td>
    
    <td align="right">
      <strong x-id="1">50</strong>
    </td>
    
    <td align="right">
      <strong x-id="1">50</strong>
    </td>
  </tr>
  
  <tr>
    <td align="left">
      <nobr>September 8</nobr>
    </td>
    
    <td align="left">
      Developer <strong x-id="1">B</strong> pushes a commit to repository <strong x-id="1">X</strong> for the first time. Developer <strong x-id="1">B</strong>'s usage is pro-rated, because the developer began contributing to repository <strong x-id="1">X</strong> partway through the month.
    </td>
    
    <td align="right">
      <sub>_50 + 1_</sub></br><strong x-id="1">51</strong>
    </td>
    
    <td align="right">
      <sub>_50 + 0.8_</sub><br/><strong x-id="1">50.8</strong>
    </td>
  </tr>
  
  <tr>
    <td align="left">
      October and November
    </td>
    
    <td align="left">
      Developer <strong x-id="1">A</strong>'s contributions to repository <strong x-id="1">X</strong> continue to count because the contributions were within the past 90 days. {% data variables.product.company_short %} now bills for developer <strong x-id="1">B</strong> for the entire month because developer <strong x-id="1">B</strong> now has contributions within the past 90 days.
    </td>
    
    <td align="right">
      <strong x-id="1">51</strong>
    </td>
    
    <td align="right">
      <strong x-id="1">51</strong>
    </td>
  </tr>
  
  <tr>
    <td align="left">
      <nobr>December 4</nobr>
    </td>
    
    <td align="left">
      90 days have passed since developer <strong x-id="1">A</strong>'s last contribution to repository _X. The 90 days lapsed after December started, so {% data variables.product.company_short %} bills for developer <strong x-id="1">A</strong> for the entire month.
    </td>
    
    <td align="right">
      <sub>_51 - 1_</sub><br/><strong x-id="1">50</strong>
    </td>
    
    <td align="right">
      <sub></sub><br/><strong x-id="1">51</strong>
    </td>
  </tr>
  
  <tr>
    <td align="left">
      <nobr>December 11</nobr>
    </td>
    
    <td align="left">
      Developer <strong x-id="1">C</strong> joins the company and pushes a commit to repository <strong x-id="1">X</strong> for the first time. Developer <strong x-id="1">C</strong>'s usage is pro-rated at 70% for 21 out of 30 days.
    </td>
    
    <td align="right">
      <sub>_50 + 1_</sub><br/><strong x-id="1">51</strong>
    </td>
    
    <td align="right">
      <sub>_51 + .07_</sub><br/><strong x-id="1">51.7</strong>
    </td>
  </tr>
  
  <tr>
    <td align="left">
      <nobr>January</nobr>
    </td>
    
    <td align="left">
      {% data variables.product.company_short %} no longer bills for developer <strong x-id="1">A</strong>. {% data variables.product.company_short %} bills for developer <strong x-id="1">C</strong> for the entire month.
    </td>
    
    <td align="right">
      <strong x-id="1">51</strong>
    </td>
    
    <td align="right">
      <strong x-id="1">51</strong>
    </td>
  </tr>
  
  <tr>
    <td align="left">
      <nobr>February 15</nobr>
    </td>
    
    <td align="left">
      A member of your enterprise disables {% data variables.product.prodname_GH_advanced_security %} for repository <strong x-id="1">X</strong>. The 51 contributors to repository <strong x-id="1">X</strong> do not work in any other repositories with {% data variables.product.prodname_GH_advanced_security %}. {% data variables.product.company_short %} bills for the developers' usage in repository <strong x-id="1">X</strong> for February.
    </td>
    
    <td align="right">
      <sub>_51 - 51_</sub><br/><strong x-id="1">0</strong>
    </td>
    
    <td align="right">
      <sub></sub><br/><strong x-id="1">51</strong>
    </td>
  </tr>
  
  <tr>
    <td align="left">
      <nobr>March</nobr>
    </td>
    
    <td align="left">
      No repository owned by your enterprise has {% data variables.product.prodname_GH_advanced_security %} enabled.
    </td>
    
    <td align="right">
      <strong x-id="1">0</strong>
    </td>
    
    <td align="right">
      <strong x-id="1">0</strong>
    </td>
  </tr>
</table>

## Getting the most out of {% data variables.product.prodname_GH_advanced_security %}

{% data reusables.advanced-security.getting-the-most-from-your-license %}
