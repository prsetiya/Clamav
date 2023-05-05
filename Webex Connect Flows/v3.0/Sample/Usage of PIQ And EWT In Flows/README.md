

# PIQ And EWT Sample Flows Overview :
- This example demonstrates the usage of PIQ and EWT node using Live Chat Flow. However, the use case is not limited to the livechat only. Any workflow can use the PIQ and EWT node.
## PIQ and EWT
- Position in the Queue (PIQ) provides the contact's current position in the selected queue.
- Estimated Wait Time (EWT) provides an estimated waiting time or the average wait time for the contact before talking to an agent.
- PIQ and EWT node can be placed only after the Queue Task node.
- For more details on PIQ and EWT please refer to the below documentation.
- https://help.imiconnect.io/docs/piq-and-ewt
- Example of PIQ and EWT node.

  <img width="800" alt="Screen Pop" src="PIQEWT.png">

The folder includes the following sample flow :
## Media Specific Workflow :
- ### Live Chat Inbound Sample Flow with PIQ and EWT :
    - Every inbound customer message sent over the configured customer chat widget will trigger this workflow.
    - This workflow represents a typical use case for a bank, where a customer reaches out to customer support executives for issues with credit cards, debit cards, savings accounts, or loan enquiry.
    - The customer selects the issue type from the pre-chat form dropdown.
    - The customer can also provide a short description of the issue.
    
## Quick Start on Workflows
1. Import the flows in your Webex Connect Service.
2. Create a chat widget template like the one shown in this picture.<img width="1266" alt="Screenshot 2022-07-14 at 5 28 57 PM" src="https://user-images.githubusercontent.com/109220058/178982103-69f0fefe-d437-485e-b9ef-5355d034fab4.png">
   Use this template in the Form Template field in the Pre-chat form and Receive Node.
3. Select the appropriate queue in the "Queue Task" node for the channel.
4. Make the flow live with the configured asset.

## PIQ and EWT Node
- We can place this node anywhere after Queue Task node in the main flows.
- The method name for PIQ and EWT node is Fetch Position in Queue.
- In the QueueID we have filled $(queue). queue is a magic variable. Value of queue comes automatically.
- If there are no contacts in the queue and the customer contact is directly assigned to the agent then the customer will get piq as -1.
- If you don't want to show piq value as -1 then you can add a branch to check if the value is not -1 then show the value of piq otherwise don't display anothing related to piq.
   
  <img width="800" alt="Screen Pop" src="PIQEWT.png">