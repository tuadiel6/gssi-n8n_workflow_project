# Data Manipulation in the Workflow Automation Tools

Data manipulation is the main type of process targeted by workflow automation tools (WAT). With the help of a motivating example, we explore data manipulation using a workflow automation tool called <a href="https://n8n.io/">N8N</a>.

## Motivating Example

<p align="justify">
The departments of a University have international collaborations with professors and researchers that can be invited to visit the hosting research group for various reasons, e.g., for giving a course or for invited visiting positions. A university faculty member can open an “invited guest position” on a system where he/she must express related information. This info can be related to the guest position, period of staying, title of collaboration, hours of lectures, and course title. The remuneration can be calculated according to the department's rules and period of staying and collaboration. After this information has been set up, an invitation letter must be generated and possibly sent to the invitee to specify the economic treatment and all the info that can be useful and used by the invitee to motivate his/her visit. 
As long as we specify the title of the course, the dates, and an abstract, a web page can be generated and published online to announce the course or the novel collaboration. Concerning the payment, when a new guest is invited, a new payment must be emitted, and this should be managed by another system when the collaboration  has been completed and confirmed.
</p>

## The proposed Solution

<p align="justify">
Nodes are the key building blocks of a workflow in N8N, and they can be used to perform a range of actions, including starting the workflow, fetching or sending data to the next
node, and manipulating data. We show how to implement the motivating example with N8N tool.
</p>

<p align="justify">The following figure shows the metamodel engineered starting from the domain specification and an exemplary instance regarding the Guest Invitation process of a University
</p>
<img src="https://github.com/tuadiel6/gssi-n8n_workflow_project/blob/main/Figures/Figures/Workflow.png" >
<p align="center"> Fig.1. Workflow</p>
