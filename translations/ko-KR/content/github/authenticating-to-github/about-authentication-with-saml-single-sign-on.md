---
title: About authentication with SAML single sign-on
intro: 'You can access {% if currentVersion == "github-ae@latest" %}{% data variables.product.product_location %}{% elsif currentVersion == "free-pro-team@latest" %}an organization that uses SAML single sign-on (SSO){% endif %} by authenticating {% if currentVersion == "github-ae@latest" %}with SAML single sign-on (SSO) {% endif %}through an identity provider (IdP).{% if currentVersion == "free-pro-team@latest" %}To authenticate with the API or Git on the command line when an organization enforces SAML SSO, you must authorize your personal access token or SSH key.{% endif %}'
product: '{% data reusables.gated-features.saml-sso %}'
redirect_from:
  - /articles/about-authentication-with-saml-single-sign-on
versions:
  free-pro-team: '*'
  github-ae: '*'
---

{% if currentVersion == "github-ae@latest" %}

SAML SSO allows an enterprise owner to centrally control and secure access to {% data variables.product.product_name %} from a SAML IdP. When you visit {% data variables.product.product_location %} in a browser, {% data variables.product.product_name %} will redirect you to your IdP to authenticate. After you successfully authenticate with an account on the IdP, the IdP redirects you back to {% data variables.product.product_location %}. {% data variables.product.product_name %} validates the response from your IdP, then grants access.

{% data reusables.saml.you-must-periodically-authenticate %}

If you can't access {% data variables.product.product_name %}, contact your local enterprise owner or administrator for {% data variables.product.product_name %}. You may be able to locate contact information for your enterprise by clicking **Support** at the bottom of any page on {% data variables.product.product_name %}. {% data variables.product.company_short %} and {% data variables.contact.github_support %} do not have access to your IdP, and cannot troubleshoot authentication problems.

{% endif %}

{% if currentVersion == "free-pro-team@latest" %}

{% data reusables.saml.dotcom-saml-explanation %} Organization owners can invite your user account on {% data variables.product.prodname_dotcom %} to join their organization that uses SAML SSO, which allows you to contribute to the organization and retain your existing identity and contributions on {% data variables.product.prodname_dotcom %}.

When you access resources within an organization that uses SAML SSO, {% data variables.product.prodname_dotcom %} will redirect you to the organization's SAML IdP to authenticate. After you successfully authenticate with your account on the IdP, the IdP redirects you back to {% data variables.product.prodname_dotcom %}, where you can access the organization's resources.

{% data reusables.saml.outside-collaborators-exemption %}

If you have recently authenticated with your organization's SAML IdP in your browser, you are automatically authorized when you access a {% data variables.product.prodname_dotcom %} organization that uses SAML SSO. If you haven't recently authenticated with your organization's SAML IdP in your browser, you must authenticate at the SAML IdP before you can access the organization.

{% data reusables.saml.you-must-periodically-authenticate %}

To use the API or Git on the command line to access protected content in an organization that uses SAML SSO, you will need to use an authorized personal access token over HTTPS or an authorized SSH key. {% data variables.product.prodname_oauth_app %} access tokens are authorized by default.

If you don't have a personal access token or an SSH key, you can create a personal access token for the command line or generate a new SSH key. For more information, see "[Creating a personal access token](/github/authenticating-to-github/creating-a-personal-access-token)" or "[Generating a new SSH key and adding it to the ssh-agent](/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)."

To use a new or existing personal access token or SSH key with an organization that enforces SAML SSO, you will need to authorize the token or authorize the SSH key for use with a SAML SSO organization. For more information, see "[Authorizing a personal access token for use with SAML single sign-on](/articles/authorizing-a-personal-access-token-for-use-with-saml-single-sign-on)" or "[Authorizing an SSH key for use with SAML single sign-on](/articles/authorizing-an-ssh-key-for-use-with-saml-single-sign-on)."

You must have an active SAML session each time you authorize an {% data variables.product.prodname_oauth_app %}.

{% endif %}

### ??? ????????????

{% if currentVersion == "free-pro-team@latest" %}- "[About identity and access management with SAML single sign-on](/github/setting-up-and-managing-organizations-and-teams/about-identity-and-access-management-with-saml-single-sign-on)"{% endif %}
{% if currentVersion == "github-ae@latest" %}- "[About identity and access management for your enterprise](/admin/authentication/about-identity-and-access-management-for-your-enterprise)"{% endif %}
