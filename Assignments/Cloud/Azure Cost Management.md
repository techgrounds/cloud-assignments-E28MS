## Subject

A frequently mentioned advantage of the cloud is that you only pay for what you use. This concerns OPEX instead of CAPEX expenses. The “Cost Management + Billing” tool provides insight into your expenses in Azure and allows you to manage your subscriptions.

When you create a 'Free Account' or a 'Student Account', you will receive an amount from Microsoft as a gift to experiment with in Azure. Please note that after 30 days your subscription will be automatically stopped, which means that all your services that are still running will be turned off.


If you have created a 'Pay-as-you-go' subscription, there are a number of services that are always free to a certain extent. Please understand that these services are sometimes integrated with other services for which you have to pay.


Azure has the following principles to successfully reduce your costs:


*  Plan (Planning)
*  Visibility
*  Accountability
*  Optimization (Optimization)
*  Iteration
  
The Total Cost of Ownership (TCO) is used to calculate how much an infrastructure costs if it is hosted in the traditional way. 

With the TCO calculator you can compare the costs of a traditional infrastructure with the costs for the same infrastructure on Azure.

## Assignment

1.  Study:
   
1.1  The Azure principles for cost management

1.2  The conditions of the 'Free subscription'

1.3  The difference between CAPEX and OPEX.

1.4. The TCO calculator

2.  Create an alert with which you can monitor your own costs.
   
3.  Understand the options Azure offers to view your spend.
   
##  Key Terms

*Evaluated Spend* This is a  value in the Budgets table and is the cost to date within the budget period for that entity.

##  Resources

[Microsoft Learn Cost Management in Azure : Alerts](https://learn.microsoft.com/en-us/azure/cost-management-billing/costs/cost-mgt-alerts-monitor-usage-spending)

Chat GPT

[Microsoft Learn Analyze Uncexpected Charges](https://learn.microsoft.com/en-us/azure/cost-management-billing/understand/analyze-unexpected-charges#create-an-anomaly-alert)

[Learn Microsoft Tutorial Create and Manage Budgets](https://learn.microsoft.com/en-gb/azure/cost-management-billing/costs/tutorial-acm-create-budgets?tabs=psbudget)

[Comparitech Azure Cost Management](https://www.comparitech.com/net-admin/azure-cost-management/)

[Azure Well-architected Cost Optimization Principles](https://learn.microsoft.com/en-us/azure/well-architected/cost-optimization/principles)

[Cloud4C Azure Cost Optimization Best Practices](https://www.cloud4c.com/blogs/azure-cloud-cost-optimization-10-best-practices

[Learn Microsoft Plan to Manage Azure Costs](https://learn.microsoft.com/en-us/azure/cost-management-billing/understand/plan-manage-costs)

[Learn Microsoft Check Free Service Usage](https://learn.microsoft.com/en-us/azure/cost-management-billing/manage/check-free-service-usage)

[Azure Free Services](https://azure.microsoft.com/en-gb/pricing/free-services/)




##  Difficulties

I found it challenging to find the details of the questions.  I think this is partly because I'm unfamiliar still with navigating the Azure menu's and parsing the relevant details from the large amounts of information.

I overcame this by focussing carefully on one questions until I felt I had a good understanding before moving to the next and by time blocking each section so I kept moving forward and didn't get stuck too long on one section.

##  Results

###   Excercise 1

1.1.  Azure Cost Management Principles

1.  **Planning:**
There are Azure tools that you can use to estimate the cost before adding services.  

They are:

*  Azure pricing calculator
*  Azure price sheet
*  Azure portal

This principle emphasizes the importance of planning and forecasting your usage of Azure resources. 

By understanding your requirements upfront, you can make informed decisions about which services to use, how much capacity you need, and how to design your infrastructure efficiently.

Planning also involves considering factors such as workload patterns, growth projections, and potential cost-saving opportunities.

2. **Visibility:**
Visibility refers to the ability to monitor and track your Azure usage and spending effectively. It involves leveraging Azure's monitoring and reporting tools to gain insights into resource utilization, performance metrics, and cost trends. With greater visibility, you can identify areas of inefficiency, pinpoint cost drivers, and make data-driven decisions to optimize your spending.

3. **Accountability:**
Accountability entails assigning responsibility for cost management within your organization. It involves establishing clear roles and processes for budgeting, monitoring, and controlling Azure expenses. By fostering a culture of accountability, teams are empowered to take ownership of their resource usage, identify cost-saving opportunities, and collaborate effectively to achieve cost reduction goals.

4. **Optimization:**
Optimization involves continuously optimizing your Azure environment to maximize value and minimize costs. This includes rightsizing resources, implementing cost-effective architectures, leveraging reserved instances or Azure Hybrid Benefit, and adopting best practices for performance and efficiency. Optimization efforts should be ongoing and iterative, driven by regular reviews, analysis, and adjustments to ensure optimal resource utilization and cost-effectiveness.

6. **Iteration:**
Iteration emphasizes the iterative nature of cost management in Azure. It highlights the need for continuous improvement and adaptation to changing business needs, technology advancements, and cost dynamics. By iterating on your cost management strategies, you can adapt to evolving requirements, incorporate lessons learned, and stay proactive in identifying and implementing new opportunities for cost reduction and optimization.

In summary, these principles provide a framework for successfully reducing costs in Azure by emphasizing proactive planning, visibility, accountability, ongoing optimization, and iterative improvement. By embracing these principles, organizations can effectively manage their Azure spending while maximizing the value of their cloud investments.


1.2. Understand the Conditions of the 'Free Service:

I located the details of the free service:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/eba9be84-95c2-4f6d-8dff-2e444fc3575e)


1.3  *Capex (Capital Expenditure):*
Capex refers to investments in physical assets like buildings, machinery, or equipment that are expected to provide benefits to the business over multiple years.

These investments are typically recorded on the balance sheet and depreciated over time, meaning their costs are spread out over their useful life.

*Opex (Operational Expenditure):*

Opex refers to day-to-day expenses necessary to keep a business running, such as rent, utilities, wages, and maintenance costs.

These expenses are recorded on the income statement and are incurred regularly to maintain business operations.


###  Exceercise 2:

In order to set my cost alerts, I first investigated the set up of my account by navigating to the Cost Analysis under Cost Management:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/d4e13506-4631-45e0-bad5-9c3e0492237a

I then had a look at Budgets under Cost Management and noted that my budget was 50 euro, and that it expires on 28-06-2024:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/663ac06d-554d-43d1-ab24-d30e7ab6b1ef)




## Bonus Learning

I noted that there was an option to add AWS account, which seems like a good thing to keep in mind as I plan to learn more Cloud providers in the future.  It seems that this feature would make it easier to work in a multi-cloud environmnet
