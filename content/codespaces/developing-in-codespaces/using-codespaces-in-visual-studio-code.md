---
title: Using Codespaces in Visual Studio Code
intro: 'You can develop in your codespace directly in {% data variables.product.prodname_vscode %} by connecting the {% data variables.product.prodname_github_codespaces %} extension with your account on {% data variables.product.product_name %}.'
product: '{% data reusables.gated-features.codespaces %}'
redirect_from:
  - /github/developing-online-with-codespaces/using-codespaces-in-visual-studio-code
  - /github/developing-online-with-codespaces/connecting-to-your-codespace-from-visual-studio-code
  - /github/developing-online-with-codespaces/using-codespaces-in-visual-studio
versions:
  fpt: '*'
  ghec: '*'
type: how_to
topics:
  - Codespaces
  - Visual Studio Code
  - Developer
shortTitle: Visual Studio Code
---

 

## Prerequisites

To develop in a codespace directly in {% data variables.product.prodname_vscode %}, you must sign into the {% data variables.product.prodname_github_codespaces %} extension. The {% data variables.product.prodname_github_codespaces %} extension requires {% data variables.product.prodname_vscode %} October 2020 Release 1.51 or later.

Use the {% data variables.product.prodname_vs %} Marketplace to install the [{% data variables.product.prodname_github_codespaces %}](https://marketplace.visualstudio.com/items?itemName=GitHub.codespaces) extension. For more information, see [Extension Marketplace](https://code.visualstudio.com/docs/editor/extension-gallery) in the {% data variables.product.prodname_vscode %} documentation.


{% mac %}

{% data reusables.codespaces.click-remote-explorer-icon-vscode %}
2. Click **Sign in to view {% data variables.product.prodname_dotcom %}...**.

   ![Signing in to view {% data variables.product.prodname_codespaces %}](/assets/images/help/codespaces/sign-in-to-view-codespaces-vscode-mac.png)

3. To authorize {% data variables.product.prodname_vscode %} to access your account on {% data variables.product.product_name %}, click **Allow**.
4. Sign in to {% data variables.product.product_name %} to approve the extension.

{% endmac %}

{% windows %}

{% data reusables.codespaces.click-remote-explorer-icon-vscode %}
2. Use the "REMOTE EXPLORER" drop-down, then click **{% data variables.product.prodname_github_codespaces %}**.

   ![The {% data variables.product.prodname_codespaces %} header](/assets/images/help/codespaces/codespaces-header-vscode.png)

3. Click **Sign in to view {% data variables.product.prodname_codespaces %}...**.

   ![Signing in to view {% data variables.product.prodname_codespaces %}](/assets/images/help/codespaces/sign-in-to-view-codespaces-vscode.png)

4. To authorize {% data variables.product.prodname_vscode %} to access your account on {% data variables.product.product_name %}, click **Allow**.
5. Sign in to {% data variables.product.product_name %} to approve the extension.

{% endwindows %}

## Creating a codespace in {% data variables.product.prodname_vscode %}

{% data reusables.codespaces.creating-a-codespace-in-vscode %}

## Opening a codespace in {% data variables.product.prodname_vscode %}

{% data reusables.codespaces.click-remote-explorer-icon-vscode %}
2. Under "Codespaces", click the codespace you want to develop in.
3. Click the Connect to Codespace icon.

   ![The Connect to Codespace icon in {% data variables.product.prodname_vscode %}](/assets/images/help/codespaces/click-connect-to-codespace-icon-vscode.png)

## Changing the machine type in {% data variables.product.prodname_vscode %}

{% data reusables.codespaces.codespaces-machine-types %}

You can change the machine type of your codespace at any time.

1. In {% data variables.product.prodname_vscode %}, open the Command Palette (`shift command P` / `shift control P`).
2. Search for and select "Codespaces: Change Machine Type."

   ![Searching for a branch to create a new {% data variables.product.prodname_codespaces %}](/assets/images/help/codespaces/vscode-change-machine-type-option.png)

3. Click the codespace that you want to change.

   ![Searching for a branch to create a new {% data variables.product.prodname_codespaces %}](/assets/images/help/codespaces/vscode-change-machine-choose-repo.png)

4. Choose the machine type you want to use. 

If the codespace is currently running, a message is displayed asking if you would like to restart and reconnect to your codespace now. Click **Yes** if you want to change the machine type used for this codespace immediately. If you click **No**, or if the codespace is not currently running, the change will take effect the next time the codespace restarts.

## Deleting a codespace in {% data variables.product.prodname_vscode %}

{% data reusables.codespaces.deleting-a-codespace-in-vscode %}
