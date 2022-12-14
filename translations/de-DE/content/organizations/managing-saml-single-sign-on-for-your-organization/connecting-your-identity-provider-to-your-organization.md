---
title: Deinen Identitätsanbieter mit Deiner Organisation verbinden
intro: 'Um SAML Single Sign-On und SCIM zu verwenden, musst Du Deinen Identitätsanbieter mit Deiner {% data variables.product.product_name %}-Organisation verbinden.'
product: '{% data reusables.gated-features.saml-sso %}'
redirect_from:
  - /articles/connecting-your-identity-provider-to-your-organization
  - /github/setting-up-and-managing-organizations-and-teams/connecting-your-identity-provider-to-your-organization
versions:
  fpt: '*'
  ghec: '*'
topics:
  - Organizations
  - Teams
shortTitle: Connect an IdP
---

When you enable SAML SSO for your {% data variables.product.product_name %} organization, you connect your identity provider (IdP) to your organization. Weitere Informationen finden Sie unter „[SAML Single Sign-On für Ihre Organisation aktivieren und testen](/organizations/managing-saml-single-sign-on-for-your-organization/enabling-and-testing-saml-single-sign-on-for-your-organization)“.

You can find the SAML and SCIM implementation details for your IdP in the IdP's documentation.
- Active Directory Federation Services (AD FS) [SAML](https://docs.microsoft.com/windows-server/identity/active-directory-federation-services)
- Azure Active Directory (Azure AD) [SAML](https://docs.microsoft.com/azure/active-directory/active-directory-saas-github-tutorial) und [SCIM](https://docs.microsoft.com/azure/active-directory/active-directory-saas-github-provisioning-tutorial)
- Okta [SAML](http://saml-doc.okta.com/SAML_Docs/How-to-Configure-SAML-2.0-for-Github-com.html) und [SCIM](http://developer.okta.com/standards/SCIM/)
- OneLogin [SAML](https://onelogin.service-now.com/support?id=kb_article&sys_id=2929ddcfdbdc5700d5505eea4b9619c6) und [SCIM](https://onelogin.service-now.com/support?id=kb_article&sys_id=5aa91d03db109700d5505eea4b96197e)
- PingOne [SAML](https://support.pingidentity.com/s/marketplace-integration/a7i1W0000004ID3QAM/github-connector)
- Shibboleth [SAML](https://wiki.shibboleth.net/confluence/display/IDP30/Home)

{% note %}

**Hinweis:** Von {% data variables.product.product_name %} unterstützte Identitätsanbieter für SCIM sind Azure AD, Okta und OneLogin. {% data reusables.scim.enterprise-account-scim %} For more information about SCIM, see "[About SCIM](/organizations/managing-saml-single-sign-on-for-your-organization/about-scim)."

{% endnote %}
