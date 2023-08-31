# Snippet Extraction

The Snippet Extraction workbench stage helps extract pertinent excerpts from the source data which can be displayed as answer snippets in response to user queries. When data is processed, relevant snippets are extracted and stored along with a title and a URL. When a user queries, the generated snippets are displayed to the users.  This makes it an efficient way to find and display answer snippets. This stage can be used to configure the fields to be used for generating the answer snippets. 

Note that this stage is only used for the Extractive Model of producing answer snippets. When the Extractive Model is enabled in Answer snippets, this workbench stage is automatically added to the Index pipeline. 

![alt_text](images/answersnippets1.png "image_tooltip")

Use the following fields to configure this Workbench stage.

**Stage Name**: Give an appropriate name to the stage for easy identification.

**Stage Type**: This field refers to the type of stage. In this case, it is set to Snippet Extraction.

**Configuration**: Use this section to define the condition under which the source data undergoes the processing of this stage and the outcome of the stage.

    **Condition**: Define a condition using the field type and operator to specify the source data on which snippet extraction is to be done. For example, if you want to generate snippets only for web pages, set the field to ‘sys_content_type’, set the operator to ‘contains’ and the value as ‘web’. This implies that the only web type of file will undergo snippet extraction.  


    **Outcome**: Specify the following fields for the outcome of the stage. 


    **Source field**: Index field whose content is to be used for extracting snippets.


    **Source Title**: Field whose value is to be used as the title of the snippet.


    **Source URL**: Field whose value is to be used as the URL in the snippet. This is the URL displayed to the user at the end of the snippet. 


    In continuation of the above example, you can set ‘page_html’ as the source field, which implies that the HTML content from the page will be used to generate the snippet. Set page_title as the Source Title and page_url as the Source URL.   


    You can add one or more outcome fields using the AND button. For example, if you want to run the snippet extraction stage for content from files, web pages, and data from the connectors, you can specify the condition and the outcome as shown below. 

![alt_text](images/answersnippets2.png "image_tooltip")

!!! note
Note that currently for structured data and the FAQs, snippets are always generated by default. Hence you do not need any specific configuration to configuration for them.

>: 🗈 Note:
    Note that currently for structured data and the FAQs, snippets are always generated by default. Hence you do not need any specific configuration to configuration for them.

Testing a table

| Syntax      | Description |
| ----------- | ----------- |
| Testing long sentences here        | for structured data and the FAQs, snippets are always generated by default. Hence you do not need any specific configuration to configuration for them.        |
| Paragraph   | Text        |

This document provides information on the various releases and the corresponding feature updates and enhancements introduced in version 10.1.x of the platform.

## v10.1.8 August 06, 2023

<span style="text-decoration:underline;">Patch Release</span>

This update includes bug fixes and feature enhancements.


<table>
  <tr>
   <td><strong>FEATURE</strong>
   </td>
   <td><strong>ENHANCEMENT</strong>
   </td>
  </tr>
  <tr>
   <td>Revamped Intent Discovery Journey
   </td>
   <td>The Intent Discovery tool was introduced as a beta feature in v10 of the Platform. This powerful tool helps bot designers auto-extract popular intents from previous user conversations. It reduces the time and effort to build a virtual assistant and leads to the success of your Conversational AI Journey.
<p>
Based on valuable customer feedback, we’ve enhanced the Intent Discovery module with the following features:
<ul>

<li><strong>Project Management</strong>: Bot designers can now create up to 10 projects in the tool, offering greater flexibility to delete or reuse existing projects.

<li><strong>Homepage</strong>: The tool’s homepage now presents Extracted Intents with clear options to add new Dialogs/FAQs or train existing ones.

<li><strong>Easy Re-extraction</strong>: Bot designers can now upload additional transcripts to re-discover additional intents, enabling the efficient reuse of existing projects.

<li><strong>Additional Enhancements</strong>: Bot designers can now bookmark suitable utterances for the extracted intent for easy reference. For each Extracted Intent, all sessions and corresponding utterances contributing to the Intent are grouped properly. Also, the Actions column now presents the results of actions taken from newly discovered intents, ensuring better tracking and management.
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>Zoom Contact Center Channel
   </td>
   <td>The Platform now supports Zoom Contact Center as a channel to automate voice and messaging services using asynchronous Webhook integration. <a href="https://developer.kore.ai/docs/bots/channel-enablement/adding-the-zoom-contact-center-channel/">Learn more</a>.
   </td>
  </tr>
  <tr>
   <td>GupShup Support for WhatsApp Payment
   </td>
   <td>The Platform now supports the Whatsapp Payment Outbound message templates in the Gupshup WhatsApp Business Channel, empowering developers to build use cases based on WhatsApp Pay. <a href="https://developer.kore.ai/docs/bots/channel-enablement/adding-the-whatsapp-business-messaging-channel/#Support_for_WhatsApp_Pay">Learn more</a>.
   </td>
  </tr>
  <tr>
   <td>Manage the Push Notifications for Web/Mobile SDK Channel
   </td>
   <td>Bot designers can now selectively send push notifications for events such as “Websocket Disconnected,” “App Termination,” and “Message Delivery Failure” in the Web/Mobile SDK channel. They can also customize the push notification messages sent to the client app using the Manage Push Notifications option in the Web/Mobile SDK channel. <a href="https://developer.kore.ai/docs/bots/channel-enablement/adding-the-webmobile-client-channel/">Learn more</a>.
   </td>
  </tr>
  <tr>
   <td>Locale Definition Property for IVR
   </td>
   <td>Bot designers can now include the language and locale identifier (<em>xml:lang= “&lt;value>”</em>) in the VoiceXML file by enabling the <strong>Locale Definition</strong> property for the IVR Channel. Automatic Speech Recognition engines use the language attribute to enhance speech recognition. <a href="https://developer.kore.ai/docs/bots/bot-builder-tool/dialog-task/voice-call-properties/#Dialog_Node_Settings">Learn more</a>.
   </td>
  </tr>
</table>