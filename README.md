# Data Manipulation in the Workflow Automation Tools

Data manipulation is the main type of process targeted by workflow automation tools (WAT). With the help of a motivating example, we explore data manipulation using a workflow automation tool called <a href="https://n8n.io/">N8N</a>.

## Motivating Example

<p align="justify">
The departments of a University have international collaborations with professors and researchers that can be invited to visit the hosting research group for various reasons, e.g., for giving a course or for invited visiting positions. A university faculty member can open an “invited guest position” on a system where he/she must express related information. This info can be related to the guest position, period of staying, title of collaboration, hours of lectures, and course title. The remuneration can be calculated according to the department's rules and period of staying and collaboration. After this information has been set up, an invitation letter must be generated and possibly sent to the invitee to specify the economic treatment and all the info that can be useful and used by the invitee to motivate his/her visit. 
As long as we specify the title of the course, the dates, and an abstract, a web page can be generated and published online to announce the course or the novel collaboration. Concerning the payment, when a new guest is invited, a new payment must be emitted, and this should be managed by another system when the collaboration  has been completed and confirmed.
</p>

## The Proposed Solution

<p align="justify">
Nodes are the key building blocks of a workflow in N8N, and they can be used to perform a range of actions, including starting the workflow, fetching or sending data to the next
node, and manipulating data. We show how to implement the motivating example with the N8N tool.
</p>

> [!NOTE]
> The following figure shows workflow automation starting from node mapping data from a Notion to a node sending an invitation email to the invited guest.

<img src="https://github.com/tuadiel6/gssi-n8n_workflow_project/blob/main/Figures/flow.png" >
<p align="center"> Fig.1. Workflow</p>

**❶ <p align="justify">The validation node was tested to verify the validity of guest emails. Various email addresses, including valid and invalid ones, were inputted to assess the validation process. The results demonstrated that the validation node successfully identified valid and invalid email addresses from the EMF model as expected.</p> 
  
  The code generation was assessed using the HTML template node to generate web pages announcing upcoming courses. The EMF data model was passed as input to this node, and the resulting web page accurately reflected the provided information, including course title, dates, and abstract, was generated.

%For Model to Model (M2M) transformation, a set node, and airtable node were employed to handle payment details based on input data from the EMF model. Model to Text (M2T) transformation was examined through the generation of customized invitation letters using the Google Doc node. The necessary information, including guest details and collaboration information from the EMF model, was inputted to generate well-formatted and comprehensive invitation letters suitable for sending to the invited guests. Finally, the email node was utilized to send emails to the invited guests, providing them with relevant information from the EMF data model. The emails, along with the generated invitation letters as attachments, were successfully sent to the intended recipients.
