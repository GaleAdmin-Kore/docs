# **Debug Logs API**

To get debug logs of a specific conversation (currently supported only for IVR Channel).


<table>
  <tr>
   <td><strong>Method</strong>
   </td>
   <td>GET
   </td>
  </tr>
  <tr>
   <td><strong>Endpoint</strong>
   </td>
   <td><code>https://{{host}}/api/{{version}/{{BotID}}/debuglogs?identity={{identity}}&channelType={{channelType}}&minimumInfo=true&limit=5&offset=300&timezone={{timezone}}</code>
   </td>
  </tr>
  <tr>
   <td><strong>Content Type</strong>
   </td>
   <td><code>application/json</code>
   </td>
  </tr>
  <tr>
   <td><strong>Authorization</strong>
   </td>
   <td><code>auth: {{JWT}}</code>
<p>
See <a href="https://developer.kore.ai/docs/bots/api-guide/apis/#Generating_the_JWT_Token">How to generate the JWT Token.</a>
   </td>
  </tr>
  <tr>
   <td><strong>API Scope</strong>
   </td>
   <td>
<ul>

<li>Bot Builder: Debug Logs

<li>Admin Console: Not Applicable
</li>
</ul>
   </td>
  </tr>
</table>





## Path Parameters


<table>
  <tr>
   <td><strong>PARAMETER</strong>
   </td>
   <td><strong>DESCRIPTION</strong>
   </td>
  </tr>
  <tr>
   <td>host
   </td>
   <td>Environment URL, for example, https://bots.kore.ai
   </td>
  </tr>
  <tr>
   <td>BotID
   </td>
   <td>Bot ID. You can access it from the General Settings page of the bot.
   </td>
  </tr>
</table>





## Sample Request


```
curl -X GET \
   'https://{{host}}/api/1.1/{{BotID}}/debuglogs?identity={{id}}&channelType=ivrVoice&minimumInfo=true&limit=5&offset=300&timezone=America/New_York' \
  -H 'auth: {{YOUR_JWT_ACCESS_TOKEN}}' \
```





## Body Parameters


<table>
  <tr>
   <td><strong>PARAMETER</strong>
   </td>
   <td><strong>DESCRIPTION</strong>
   </td>
  </tr>
  <tr>
   <td>version
   </td>
   <td>Refers to the version of the API. The current version of this API is “1.1”
   </td>
  </tr>
  <tr>
   <td>identity
   </td>
   <td>Unique ID associated with the call.
   </td>
  </tr>
  <tr>
   <td>channelType
   </td>
   <td> “<strong>ivrVoice</strong>” and <strong>web/mobile client </strong>channels are currently supported.
   </td>
  </tr>
  <tr>
   <td>minimumInfo
   </td>
   <td>Optional field. Set to “true” to get only the summary.
   </td>
  </tr>
  <tr>
   <td>offset
   </td>
   <td>Specify the page number from which to start fetching the logs. If unspecified, it starts from 0, which is the first page of the list of logs.
   </td>
  </tr>
  <tr>
   <td>limit
   </td>
   <td>The number of records to fetch. The maximum applicable limit is 50.
   </td>
  </tr>
  <tr>
   <td>timezone
   </td>
   <td>Ex: America/New_York.
   </td>
  </tr>
  <tr>
   <td>fromDate
   </td>
   <td>Date from which the logs are requested, valid formats – yyyy-mm-dd or valid timestamp.
   </td>
  </tr>
  <tr>
   <td>toDate
   </td>
   <td>Date up to which the logs are requested, valid formats – yyyy-mm-dd or valid timestamp.
   </td>
  </tr>
</table>





## Sample Response


```
[
    {
        "timestamp": "2018-11-22T13:06:17.258Z",
        "nomatch_count": "0",
        "noinput_count": "1",
        "debugTitle": "Bing",
        "debugLevel": "Info",
        "debugMessage": "intent node initiated",
        "metaInfo": {
            "channel": "ivrVoice",
            "identity": "Nov22PilotEnv1"
        }
    },
    {
        "timestamp": "2018-11-22T13:06:17.258Z",
        "debugTitle": "Bing",
        "debugLevel": "Info",
        "debugMessage": "intent node processing is completed",
        "metaInfo": {
            "channel": "ivrVoice",
            "identity": "Nov22PilotEnv1"
        }
    },
    {
        "timestamp": "2018-11-22T13:06:17.258Z",
        "debugTitle": "Nam",
        "debugLevel": "Info",
        "debugMessage": "entity node initiated",
        "metaInfo": {
            "channel": "