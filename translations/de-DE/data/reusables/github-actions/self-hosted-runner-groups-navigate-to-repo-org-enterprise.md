1. Navigate to where your self-hosted runner groups are located:
   * **In an organization**: navigate to the main page and click {% octicon "gear" aria-label="The Settings gear" %} **Settings**.
   * {% ifversion fpt or ghec %}**If using an enterprise account**: navigate to your enterprise account by visiting `https://github.com/enterprises/ENTERPRISE-NAME`, replacing `ENTERPRISE-NAME` with your enterprise account's name.{% elsif ghes or ghae %}**If using an enterprise-level runner**:

     1. Klicke in der oberen rechten Ecke einer beliebigen Seite auf {% octicon "rocket" aria-label="The rocket ship" %}.
     1. In the left sidebar, click **Enterprise overview**.
     1. {% endif %} In the enterprise sidebar, {% octicon "law" aria-label="The law icon" %} **Policies**.
1. Navigate to the "Runner groups" settings:
   * **In an organization**: Click **Actions** in the left sidebar{% ifversion fpt or ghec %}, then click **Runner groups** below it{% endif %}.
   * {% ifversion fpt or ghec %}**If using an enterprise account**:{% elsif ghes or ghae %}**If using an enterprise-level runner**:{% endif %} Click **Actions** under "{% octicon "law" aria-label="The law icon" %} Policies"{% ifversion fpt or ghec %}, then click the **Runners groups** tab{% endif %}.
