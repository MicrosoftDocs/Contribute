---
title: How to use GitHub on Visual Studio
description: This article provides the basics and reference information for using github on Microsoft's Visual Studio.
ms.date: 18/08/2018
---
# Authenticating to GitHub

## How to login to GitHub or GitHub Enterprise

1. In Visual Studio, select **Team Explorer** from the **View** menu.

1. In the Team Explorer pane, click the **Manage Connectios** toolbar icon.

1. Click the **Connect** link in the GitHub section.


   If you're connected to a TFS instance, click on the **Sign in** link instead

   If none of these options are visible, click **Manage Connections** and then **Connect to GitHub**.  

1. In the **Connect to GitHub dialog** choose **GitHub** or **GitHub Enterprise**, depending on which product you're using.

**GitHub option**:

- To sign in with credentials, enter either username or email and password.
- To sign in with SSO, select `Sign in with your browser`.

**GitHub Enterprise option**:  

- To sign in with SSO, enter the GitHub Enterprise server address and select `Sign in with your browser`.
- To sign in with credentials, enter the GitHub Enterprise server address.
   - If a `Password` field appears, enter your password.
   - If a `Token` field appears, enter a valid token. You can create personal access tokens by [following the instructions in the section below](#personal_access_tokens).

Before you authenticate, you must already have a GitHub or GitHub Enterprise account.


### Personal access tokens

If all signin options above fail, you can manually create a personal access token and use it as your password.

The scopes for the personal access token are: `user`, `repo`, `gist`, and `write:public_key`.
- *user* scope: Grants access to the user profile data. We currently use this to display your avatar and check whether your plans lets you publish private repositories.
- *repo* scope: Grants read/write access to code, commit statuses, invitations, collaborators, adding team memberships, and deployment statuses for public and private repositories and organizations. This is needed for all git network operations (push, pull, fetch), and for getting information about the repository you're currently working on.
- *gist* scope: Grants write access to gists. We use this in our gist feature, so you can highlight code and create gists directly from Visual Studio
- *write:public_key* scope: Grants access to creating, listing, and viewing details for public keys. This will allows us to add ssh support to your repositories, if you are unable to go through https (this feature is not available yet, this scope is optional)
