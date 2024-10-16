# Audit Logs

On the **Settings** console, you can monitor events related to your account's modules **and actions taken by the users linked to your account**. 

**Audit Logs** offer a comprehensive and time-based view of all the account events. Each log entry includes:

- Event name and category.
- The user who performed the action.
- Date and time of the event.
- Detailed description of the action.

<img src="../images/audit-logs-metadata.png" alt="audit logs metadata" title="audit logs metadata" style="border: 1px solid gray; zoom:75%;">

The event metadata provides business users with actionable insights, helping them in efficiently identifying patterns in user activities within their accounts. It also aids in detecting anomalies, spotting unauthorized usage, and enhancing overall account security.

You can specify a **current** or **past period** to view the logs and have complete visibility into the activities and modifications in your account. [Learn more](./audit-logs.md/#steps-to-set-time-range-for-audit-logs){:target="_blank"}.

Additionally, you can set **custom filters** based on a specific category, event, or user value to view only the required audit logs. [Learn more](./audit-logs.md/#steps-to-add-a-custom-filter){:target="_blank"}.

<div class="admonition note">
<p class="admonition-title">Note</p>
<p><ul><li>The <b>IP Address</b> is fetched from the user’s current network.</li>
<li><b>User ID</b>, <b>Role ID</b>, <b>Model ID</b>, <b>Agent ID</b>, <b>Guardrail ID</b>, <b>Integration ID</b>, and <b>Experiment ID</b> pertain to the unique identifier associated with the module’s entity in the system.</li></ul></p></div>

<div class="admonition warning">
<p class="admonition-title">Universal Metadata</p>
<p>The <b>User ID</b> and <b>IP Address</b> are shown for audit log entries across all modules, in addition to module and category specific metadata listed in the tables below.</p></div>

<table>
    <tr>
   <td colspan="3" align="center"><strong>Category</strong>: Login/Logout
   </td>
  </tr>
  <tr>
   <td colspan="3" ><b>Metadata</b>: <strong><i>Email ID</i></strong> is displayed for all the category events below.
   </td>
  </tr>
    <tr>
   <td><strong>Event</strong>
   </td>
   <td><strong>Description</strong>
   </td>
   <td><strong>Additional Metadata</strong>
   </td>
  </tr>
  <tr>
   <td>Login
   </td>
   <td>Tracks the account login activity.
   </td>
   <td>
<ul>
<li>Login method
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>Logout
   </td>
   <td>Tracks the account logout activity.
   </td>
   <td align="center">
    -
   </td>
  </tr>
  </table>

  <table>
  <tr>
     <td colspan="3" align="center"><strong>Category</strong>: Roles
   </td>
   </tr>
  <tr>
   <td colspan="3"><b>Metadata</b>: <strong><i>Role ID</i></strong> is displayed for all the category events below, except <em>Role Changed</em>.
   </td>
  </tr>
      <tr>
   <td><strong>Event</strong>
   </td>
   <td><strong>Description</strong>
   </td>
   <td><strong>Additional Metadata</strong>
   </td>
  </tr>
  <tr>
          <td>Role edited
   </td>
   <td>Tracks the edits done to a custom role.
   </td>
   <td align="center">
    -
   </td>
  </tr>
  <tr>
   <td>Role created
   </td>
   <td>Tracks the creation of custom roles.
   </td>
   <td rowspan="2" >
<ul>
<li>Role Type
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>Role deleted
   </td>
   <td>Tracks the deletion of custom roles.
   </td>
  </tr>
  <tr>
   <td>Role changed
   </td>
   <td>Tracks the role changes made for member users. This also includes role  changes for multiple users (bulk change).
   </td>
   <td align="center">
    -
   </td>
  </tr>
  </table>

  <table>
  <tr>
     <td colspan="3" align="center"><strong>Category</strong>: Integrations
   </td>
   </tr>
  <tr>
  <td colspan="3"><b>Metadata</b>: <b><i>Integration Name</i></b>, <b><i>Integration ID</i></b>, and <b><i>Integration Type</i></b> are displayed for all the category events below.</td></tr>
        <tr>
   <td><strong>Event</strong>
   </td>
   <td><strong>Description</strong>
   </td>
   <td><strong>Additional Metadata</strong>
   </td>
  </tr>
  <tr>
   <td>Integration added
   </td>
   <td>Tracks integrations added by the user to the account.
   </td>
   <td rowspan="2" align="center">-</td>
   </tr>
  <tr>
   <td>Integration deleted
   </td>
   <td>Tracks integration deletions in the account.
   </td>
  </tr>
  </table>

  <table>
  <tr>
     <td colspan="3" align="center"><strong>Category</strong>: Models
   </td>
   </tr>
  <tr>
   <td colspan="3">
   <p><b>Metadata</b>:</p>
<ul>
<li><strong><i>Model ID</i></strong> and <strong><i>Model Name</i></strong> are displayed for all the <em>Model</em> category events.
<li><strong><i>Model Type</i></strong> is displayed for <em>Model Deleted</em>, <em>API Key created</em>, <em>API Key deleted</em>, <em>Model Finetuning</em>, <em>Model Deployed</em>, and <em>Model Undeployed </em>events.
<li><strong><i>Hardware Type</i></strong> is displayed for <em>Model Finetuning</em>, <em>Model Deployed</em>, and <em>Model Undeployed</em> events.
</li>
</ul>
   </td>
  </tr>
   <tr>
   <td><strong>Event</strong>
   </td>
   <td><strong>Description</strong>
   </td>
   <td><strong>Additional Metadata</strong>
   </td>
  </tr>
  <tr>
   <td>Model added(external models only)
   </td>
   <td>Tracks the addition of external models to the account.
   </td>
   <td rowspan="4" align="center">
   -
   </td>
  </tr>
  <tr>
   <td>Model deleted
   </td>
   <td>Tracks the deletion of external models from the account.
   </td>
  </tr>
  <tr>
   <td>API Key created
   </td>
   <td>Tracks the creation of an API key for a model in the account.
   </td>
  </tr>
  <tr>
   <td>API Key deleted
   </td>
   <td>Tracks the deletion of an API key for a model by the account user.
   </td>
  </tr>
  <tr>
   <td>Model Finetuning
   </td>
   <td>Tracks the finetuning process for models done by the account user.
   </td>
   <td>
<ul>
<li>Training method

<li>No. of epochs

<li>Batch size

<li>Learning rate

<li>Training dataset

<li>Test dataset

<li>Weights and Biases
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>Model deployed
   </td>
   <td>Tracks the open-source model deployments in the account.
   </td>
   <td>
<ul>

<li>Temperature

<li>Max length

<li>Top p

<li>Top k

<li>Stop Sequence

<li>Inference batch size

<li>Min Replicas

<li>Max Replicas

<li>Scale up Delay

<li>Scale down Delay
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>Model undeployed
   </td>
   <td>Tracks the opensource model undeployments in the account.
   </td>
   <td>
<ul>

<li> Hours of usage

<li> Temperature

<li>Max length

<li>Top p

<li>Top k

<li> Stop sequence

<li>Inference batch size

<li>Min replicas

<li>Max replicas

<li>Scale up delay

<li>Scale down delay
</li>
</ul>
   </td>
  </tr>
  </table>

  <table>
  <tr>
     <td colspan="3" align="center"><strong>Category</strong>: Agents
   </td>
   </tr>
  <tr>
   <td colspan="3"><b>Metadata</b>: <strong><i>Agent ID</i></strong> and <strong><i>Agent Name</i></strong> are displayed for all the category events below.
   </td>
  </tr>
     <tr>
   <td><strong>Event</strong>
   </td>
   <td><strong>Description</strong>
   </td>
   <td><strong>Additional Metadata</strong>
   </td>
  </tr>
  <tr>
   <td>Agent created
   </td>
   <td>Tracks the creation of an agent in the account.
   </td>
   <td align="center">
   -
   </td>
  </tr>
  <tr>
   <td>Agent deleted
   </td>
   <td>Tracks the deletion of an agent in the account.
   </td>
   <td>
<ul>

<li>Model ID

<li>Model Name

<li>Model Type
</li>
</ul>
   </td>
  </tr>
  </table>

  <table>
    <tr>
     <td colspan="3" align="center"><strong>Category</strong>: Users Management
   </td>
   </tr>
      <tr>
   <td><strong>Event</strong>
   </td>
   <td><strong>Description</strong>
   </td>
   <td><strong>Additional Metadata</strong>
   </td>
  </tr>
  <tr>
   <td>User invited
   </td>
   <td>Tracks the invitation of new users to the account.
   </td>
   <td>
<ul>
<li>Added User IDs
<li>Role Name

<li>Role ID
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>User deleted
   </td>
   <td>Tracks the deletion of existing users from the account.
   </td>
   <td>
<ul>
<li>Removed User IDs
</li>
</ul>
   </td>
  </tr>
  </table>

  <table>
      <tr>
     <td colspan="3" align="center"><strong>Category</strong>: Prompts
   </td>
   </tr>
  <tr>
   <td colspan="3">
   <p><b>Metadata</b>:</p>
<ul>
<li><strong><i>Prompt ID</i></strong> is displayed for all the <em>Prompts </em>category events.
<li><strong><i>Prompt Name</i></strong> is displayed for <em>Prompt created</em>, <em>Versions Committed</em>, <em>Versions Restored</em>, <em>Prompt Shared</em>, <em>Endpoint Copied</em>, and <em>API Key Created </em>category events.
</li>
</ul>
   </td>
  </tr>
   <tr>
   <td><strong>Event</strong>
   </td>
   <td><strong>Description</strong>
   </td>
   <td><strong>Additional Metadata</strong>
   </td>
  </tr>
  <tr>
   <td>Prompt created
   </td>
   <td>Tracks the creation of a prompt by the account user.
   </td>
   <td rowspan="2" align="center">
   -
   </td>
  </tr>
  <tr>
   <td>Prompt deleted
   </td>
   <td>Tracks the deletion of a prompt by the account user.
   </td>
  </tr>
  <tr>
   <td>Versions committed
   </td>
   <td>Tracks the prompt versions committed by the account user.
   </td>
   <td rowspan="2" >
<ul>
<li>Version Name
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>Version Restored
   </td>
   <td>Tracks the prompt version restored by the account user.
   </td>
  </tr>
  <tr>
   <td>Prompt Shared
   </td>
   <td>Tracks the prompts shared by the account user with other users.
   </td>
   <td rowspan="3" align="center">
   -
   </td>
  </tr>
  <tr>
   <td>Endpoint Copied
   </td>
   <td>Tracks the prompt endpoint copy done by the account user.
   </td>
  </tr>
  <tr>
   <td>API Key Created
   </td>
   <td>Tracks the API key creation for the prompt endpoint by the account user.
   </td>
  </tr>
  <tr>
   <td>Generated Test Data
   </td>
   <td>Tracks the generation of test data by the account user.
   </td>
   <td rowspan="2" >
<ul>

<li>Model name

<li>Model ID

<li>Tokens Consumed
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>Generated Prompt
   </td>
   <td>Tracks the prompt generation done by the accout user.
   </td>
  </tr>
  </table>

  <table>
      <tr>
     <td colspan="3" align="center"><strong>Category</strong>: Dataset
   </td>
   </tr>
   <tr>
   <td><strong>Event</strong>
   </td>
   <td><strong>Description</strong>
   </td>
   <td><strong>Additional Metadata</strong>
   </td>
  </tr>
  <tr>
   <td>Dataset uploaded
   </td>
   <td>Tracks the dataset uploads in the account.
   </td>
   <td>
<ul>
<li>File type(extension)
</li>
</ul>
   </td>
  </tr>
  </table>

  <table>
     <tr>
     <td colspan="3" align="center"><strong>Category</strong>: Guardrails
   </td>
   </tr>
   <tr>
   <td colspan="3">
   <b>Metadata</b>: <strong><i>Guardrail Name</i></strong>, <strong><i>Guardrail ID</i></strong>, and <strong><i>Hardware Type</i></strong> are displayed for all the category events below.
   </td>
  </tr>
  <tr>
   <td><strong>Event</strong>
   </td>
   <td><strong>Description</strong>
   </td>
   <td><strong>Additional Metadata</strong>
   </td>
  </tr>
  <tr>
   <td>Guardrails deployed
   </td>
   <td>Tracks the guardrails deployment in the account.
   </td>
   <td align="center">
    -
   </td>
  </tr>
  <tr>
   <td>Guardrails undeployed
   </td>
   <td>Tracks the guardrails undeployment in the account.
   </td>
   <td>
<ul>

<li>Time of Usage
</li>
</ul>
   </td>
  </tr>
</table>

## Access Audit Logs

To access and view audit logs, follow the steps below:

1. [Sign in](https://galeadmin-kore.github.io/docs/gale/getting-started/sign-up-sign-in/#sign-in-to-gale){:target="_blank"} to your GALE account.
2. Navigate to the [Settings](https://galeadmin-kore.github.io/docs/gale/settings/settings-overview/#access-settings-console){:target="_blank"} console.
3. Click **Monitoring** > **Audit Logs** on the left navigation menu.
<img src="../images/access-audit-logs.png" alt="access audit logs" title="access audit logs" style="border: 1px solid gray; zoom:75%;">

## Audit Logs Information

The **Audit Logs** Dashboard displays the following information to collectively provide a comprehensive overview of activities within your GALE account:

* **Event Name:** Describes the specific event or action that occurred.
* **Category:** Identifies the module or entity affected by the event.
* **User Name:** Specifies the name of the user who performed the action or triggered the event.
* **Date and Time:** Represents when the event occurred.
* **Description:** Provides detailed information about what was done.
<img src="../images/audit-logs-dashboard.png" alt="audit logs dashboard" title="audit logs dashboard" style="border: 1px solid gray; zoom:75%;">

## Filter Audit Logs

You can narrow down the information displayed in your account's audit logs by applying custom filters. 

These filters allow you to select specific categories, events, or users and then apply operators like **Is** **Equal To** or **Is Not Equal To** to specify the desired value. 

This customization helps you focus on relevant audit logs, making it easier to track or investigate specific actions or users within your account.

### Steps to Add a Custom Filter

1. Navigate to the **Audit Logs** dashboard.
2. Click the **Filter** icon.
3. Click **+Add Filter**.
<img src="../images/add-filter-audit-logs.png" alt="add filter" title="audit logs" style="border: 1px solid gray; zoom:75%;">

4. In the **Filter By** window, select the required option from the dropdown list for **Select Column**, **Select Operator**, and **Enter Value**.
<img src="../images/select-filter-from-dropdown.png" alt="select filter" title="select filter" style="border: 1px solid gray; zoom:75%;">

<div class="admonition note">
<p class="admonition-title">Note</p>
<p>When you use "<b>Is Equal To</b>," the audit logs only show entries that match the specified value. Conversely, when you use "<b>Is Not Equal To</b>," the logs display all entries except those that match the specified value.</p></div>

For example, applying the filter <b>Event Is Equal To Role Created</b>, as shown below, displays only the logs for the role creation event.

<img src="../images/example-filter.png" alt="example filter" title="example filter" style="border: 1px solid gray; zoom:75%;">

To view the logs for all the events except role creation, you must set the filter as follows:

<img src="../images/view-all-logs.png" alt="view all logs" title="view all logs" style="border: 1px solid gray; zoom:75%;">

5. Click **Apply**.

All the log entries relevant to the applied filter(s) are displayed, as shown below.
<img src="../images/log-entries.png" alt="log entries" title="log entries" style="border: 1px solid gray; zoom:75%;">

To clear the filter settings, click **Clear All**.

<img src="../images/clear-all-filters.png" alt="clear all fllters" title="clear all fllters" style="border: 1px solid gray; zoom:75%;">

The number of filters you have applied is displayed on the **Filter** icon.
<img src="../images/applied-filters.png" alt="applied filters" title="applied filters" style="border: 1px solid gray; zoom:75%;">

### Add Multiple Filters

You can enhance your audit log visibility by adding multiple filters. This capability allows you to specify detailed criteria such as specific categories, events, or users, enabling you to obtain fine-grained results. 

By combining filters, you can precisely focus on and analyze the audit log entries that are most relevant to your requirements.

When adding multiple filters to refine your audit log queries, you can use the **AND** or **OR** operators in multiple filtering steps effectively. 

<div class="admonition note">
<p class="admonition-title">Note</p>
<p>Consistency in operator usage is required for each filtering step. This means you need to use either the AND operator or the OR operator throughout all criteria.

Both operators cannot be used together.</p></div>

<img src="../images/operators-mutually-exclusive.png" alt="mutually exclusive operators" title="mutually exclusive operators" style="border: 1px solid gray; zoom:75%;">

Using the AND operator ensures that all specified conditions must be met for an entry to be included in the results. 

On the other hand, using the OR operator broadens the criteria, allowing entries that meet any of the specified conditions to be included. These operators provide flexibility in tailoring your audit log views.

#### Steps to Add Multiple Filters

1. Follow **Steps 1 to 3** mentioned [here](./audit-logs.md/#steps-to-add-a-custom-filter){:target="_blank"}.
2. Select the **AND/OR** operator tab in the **Filter by** window.

    <img src="../images/filter-operators.png" alt="filter operators" title="filter operators" style="border: 1px solid gray; zoom:75%;">

3. Follow **Steps 4 to 5** mentioned [here](./audit-logs.md/#steps-to-add-a-custom-filter){:target="_blank"}.

The matched log entries are displayed in the dashboard. 

## Time-based Audit Logs

You can view and monitor audit logs within a specific period with the time selection feature. This capability allows you to focus on audit log entries that occurred within a defined time-frame, and track changes.

Time selection is available for past and current time periods, including the ones listed below:

<div class="admonition note">
<p class="admonition-title">Note</p>
<p><b>Last 30 Days</b> is the default selection, which displays logs for the past 30 days from the current date.</p></div>

* **All Time**: Displays logs since the time the account was created.
* **Today**: Includes audit logs generated on the current day.
* **Yesterday**:  Includes audit logs generated on the previous day.
* **This Week**: Displays logs for all the days in the current week.
* **This Month**: Displays logs for all the days in the current month.
* **Last Month**: Displays logs for all the days in the previous month.
* **Last 30 Days**: Displays logs for the past 30 days from the current date, if events’ data exists.
* **Last 90 Days**: Displays logs for the past 90 days from the current date.
* **This Year**: Displays logs for all the days in the current year.
* **Last Year**: Displays logs for all the days in the past year.

### Steps to Set Time Range for Audit Logs

1. [Navigate](./audit-logs.md/#access-audit-logs){:target="_blank"} to the **Audit Logs** dashboard.
2. Click the time selection button (displays **Last 30 Days**).
<img src="../images/click-time-selection.png" alt="time selection" title="time selection" style="border: 1px solid gray; zoom:75%;">

3. Select the required period on the left panel, or select a specific date, month or year on the calendar widget (the current day is the default selection).
4. Click **Apply**.
<img src="../images/apply-changes.png" alt="apply changes" title="apply changes" style="border: 1px solid gray; zoom:75%;">

The audit logs for events that occurred within the selected time period are displayed. 

### Key Considerations and Tips

The time range is automatically selected on the calendar widget once you select the period. Also, the date range is displayed at the bottom of the widget.

<img src="../images/time-range-display.png" alt="time range display" title="time range display" style="border: 1px solid gray; zoom:75%;">

You can select a specific month or year from the relevant dropdown list and switch to different months by clicking the **forward/backward** arrows.

<img src="../images/forward-back-arrows.png" alt="pagination arrows" title="pagination arrows" style="border: 1px solid gray; zoom:75%;">

To set a specific date as the start date for viewing audit logs, click on the desired date in the widget. 

By default, the current day will be set as the end date. This feature allows you to easily customize the period for which you want to monitor and analyze audit logs.

<img src="../images/custom-start-date.png" alt="custom start date" title="custom start date" style="border: 1px solid gray; zoom:75%;">

For more help or information on <b>Audit Logs</b>, [contact](https://kore.ai/support/){:target="_blank"} our technical support team.

[Learn more](../settings-overview.md){:target="_blank"} about other features on the <b>Settings</b> Console.
