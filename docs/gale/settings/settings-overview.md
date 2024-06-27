# Settings Console Overview

GALE’s **Settings** console is a centralized management interface that provides administrators with the tools and functionalities to configure, monitor, and manage GALE’s system configurations to manage the following:

* Users
* Roles and permissions
* Automated synchronization of user data from Enterprise AD, plus configuration of user profile fields and email notifications.
* Integrations
* Manage Guardrails 

## Levels of Users Management 

The **Settings** Console provides administrators comprehensive control and visibility on the user management features available at the account and agent levels, facilitating proactive and improved management.

* **Account level**: At the account level, administrators can manage users, integrations, and security permissions with a broader scope, encompassing the entire GALE account. This includes responsibilities such as user registration, access control, and permissions applicable across various applications within the GALE platform. The list of configured integrations can also be managed at the account level.
* **Agent level**: User management becomes more detailed and specific at the agent level, concentrating on individual agent deployments and configurations within the GALE platform. The owner of each respective agent holds the authority to extend invitations to any number of individual users and customize their permissions and access levels for creating and deleting an agent, assigning roles, and managing deployments, guardrail configurations, and API keys.

This post describes how to access the **Settings Console** and summarizes the modules and features available.

<div class="admonition note">
<p class="admonition-title">Note</p>
<p>Only users included as Admin in the system with the required permissions can access the Settings Console.</p>
</div>

## What You Can Do on the Settings Console

For modules defined on the Settings Console, you can do the following:

**Users**

* Add a new user to your account via email invitation or user information file import.
* View the summary of counts for total, active, inactive, and locked users.
* View the list of all the users in your account and their details like Name, Email ID, Account Role, and Status.
* Select and delete one or multiple users from your account.
* Unlock locked users.

**Roles and Permissions**

* View system-generated roles for <b>account</b> and <b>agent</b> role types.
* Duplicate the roles and make custom changes.
* View the enabled/disabled access controls for various modules and permissions for system roles.
* Add new custom roles for agent and account types, enable/disable access, and set access controls (full, view, custom, and no access) for various modules and permissions assigned to the roles.

**Settings**

* Sync and import key user information from your organization's Active Directory (AD) by doing the following:  
  * Configuring the connection to your AD.
  * Importing user data from all or specific organization units.
  * Selecting and managing default AD user fields, or adding custom fields, and defining inclusion and exclusion rules for data import and sync.
  * Configuring AD auto sync schedules to ensure user data on GALE remains up-to-date.
* View sync history and reports to monitor successful and failed AD syncs.
* Manage the ability to view and edit default and custom user data fields.
* Configure how joining requests from new users are handled, including automatic approval options.
* Choose whether users should receive email notifications upon being added to your account via email invitation or AD sync.

**Integrations**

Integrate connections for Weights & Biases, AWS S3 Bucket, and Hugging Face using API or App credentials.

**Guardrails**

Deploy and undeploy guardrail models to apply scanners to prompt input and output text across all agents.

## Access Settings Console

To access the **Settings Console** on GALE, follow the steps below:

1. Log in to GALE using your credentials.
2. Click **Settings** on the top menu.
<img src="../images/Settings-console.png" alt="click settings" title="click settings" style="border: 1px solid gray; zoom:75%;">

The system redirects to the **Users** page under **Users Management** on the **Settings** console.

## Modules and Features

The following modules and features are supported on the Settings Console:

<table>
  <tr>
   <td><strong>Module</strong>
   </td>
   <td><strong>Description</strong>
   </td>
   <td><strong>Features</strong>
   </td>
  </tr>
  <tr>
   <td><b>Users Management</b></td>
   <td><p>Helps add, remove, and manage admin, member, and viewer users, roles, and permissions for accounts, agents, and models.</p>
<p>Manage user settings for AD sync, profile visibility and configuration, self-signup for enterprise users, and email notifications to users.</p></td>
<td><p><strong>Users</strong></p>
<ul>
<li>All users across your enterprise network accounts are listed here.</li> 
<li>A summarized view of the total invited users, active, inactive, and locked users is displayed.</li>
<li>The user listing with information on all the users across the GALE accounts is displayed with the Name, Email ID, Account Role, and Status is displayed. The account owner is highlighted.</li>
<li>You can add a new user by sending bulk or individual email invites. Alternatively,  import the user information file directly to the console.</li>
<li>Set user role when sending the email invite to one of the following:
<ul>
<li>Master Admin</li>
<li>Admin</li>
<li>Member</li>
<li>Viewer</li>
<li>Custom roles</li>
</li>
<li>Select one or multiple users to change access permissions or delete a user.</li>
<li>Click a user entry to manage their profile, models, and agents, including modifying and deleting roles within each model or agent. A model or agent can be added for a specific role.</li></ul></ul>
<p><strong>Role Management</strong></p>
<ul>
<li>A summarized view of the total roles available in the system and the number of system and custom roles are displayed.</li>
<li>View, assign, and reassign system/ default or custom roles. <strong>You cannot edit or delete system roles.</strong></li>
<li>Create a copy or duplicate of a system role as a custom role and manage its permissions and access levels.</li>
<li>Add, delete, edit permissions’ access for, and duplicate custom roles.</li>
<li>For agent and account role types, assign/unassign permissions and set access levels for various module aspects like agents, models, playgrounds and experiments, billing, integrations, guardrails, security and control settings, and user management tasks.</li></ul>

<p><strong>Settings</strong></p>
<ul>
<li><strong>Active Directory</strong>: Configure and connect your organization's AD to import user information from required organization units to GALE seamlessly. Enable automatic data sync between the AD and GALE daily, weekly, or monthly.
</li>
<li><strong>User Settings</strong>: Set up the visibility of user profile information across GALE. Select profile fields and allow edits by the end user.
</li>
<li><strong>Self sign up for enterprise users</strong>: Configure if new users from your domain can request to join this account.</li>
<li><strong>Email Notifications</strong>: Select if and when the users should receive email notifications when they are added to your account.
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td><b>Integrations</b></td>
   <td>Manage the configured easy and custom integrations and connections in one place.</td>
   <td>
<ul>
<li><strong>Weights and Biases</strong>: Monitor fine-tuning model performance in WandB Console. <a href="https://galeadmin-kore.github.io/docs/gale/integrations/how-to-integrate-with-wandb/">Learn more</a>.
</li>
<li><strong>AWS S3 Bucket</strong>: Establish a connection and import files seamlessly from the required bucket. <a href="https://galeadmin-kore.github.io/docs/gale/integrations/how-to-integrate-with-s3-bucket/">Learn more</a>.</li>
<li><strong>Hugging Face</strong>: Import exclusive and private models into GALE from a vast repository of pre-trained models for various NLP tasks such as text classification, translation, summarization, question answering, and more.<a href="https://galeadmin-kore.github.io/docs/gale/integrations/how-to-enable-hugging-face/"> Learn more</a>.</li></ul>
   </td>
  </tr>
  <tr>
   <td><b>Manage Guardrails</b></td>
   <td>Deploy models to make them available for anomaly scanners in all the agents. 
   </td>
   <td>
<ul>
<li><strong>Anonymize</strong>: Prevents the exposure of sensitive information in documents, emails, messages, or any other text data in prompts using techniques like redaction, Pseudonymization, and generalization.
</li>
<li><strong>Ban Topics</strong>: Restricts sensitive and controversial topics like religion or corporate politics in prompts to maintain content moderation, enforce community guidelines, and ensure compliance with organizational policies.</li>
<li><strong>Prompt Injection</strong>: Guards against attacks where malicious input is crafted to influence the behavior of a language model, causing it to generate harmful, misleading, or unintended responses using input sanitization, context control, role-based access, instruction clarity, and more.</li>
<li><strong>Toxicity</strong>: Set up mechanisms to detect and manage toxic content, such as harmful, offensive, or abusive language. Implement warnings, content removal, or user-banning actions to prevent the dissemination of harmful content and maintain a safe and positive user environment.</li>
<li><strong>Bias Detection</strong>: Ensure fairness and inclusivity by AI agents towards users through output evaluation for systematic prejudices or pre-defined biases and behavior and automatic neutralization of responses.</li>
<li><strong>Relevance</strong>: Ensure that prompt outputs are accurate to the input context, meet the user’s intent, and satisfy their query or need. The scanner provides a confidence score to indicate the degree of context relevance.
</li>
</ul>
 </td>
  </tr>
</table>

