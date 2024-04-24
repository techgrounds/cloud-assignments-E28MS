## Subject

Azure mentions 6 benefits of cloud computing. 

These are basic properties that make the cloud interesting for companies. 

Please note that this is also a marketing tool to introduce Azure to new customers. 

That is why it is also an important part of the AZ-900 exam.

The six benefits of cloud computing are:

*  High Availability
*  Depending on the service level agreement (SLA)
*  Scalability (Both vertically and horizontally)
*  Elasticity
*  Agility
*  Geo distribution
*  Disaster recovery

  
Azure uses a consumption-based model. This means that you only pay for the resources you use. This replaces Capital Expenditure (CapEx) with Operational Expenditure (OpEx).

## Assignment

Study:

The 6 advantages of the cloud

The consumption-based model

##  Key Terms

SLA - Service Level Agreement : This is the agreement between your business and Azure, so entails what they commit to provide.

##  Resources

[AWS White Paper 6 Advantages of Cloud Computing](https://docs.aws.amazon.com/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html)

ChatGPT

[Microsoft Azure Financial Considerations](https://azure.microsoft.com/en-us/solutions/cloud-economics/#financial-considerations)

[GitHub Azure Mentor](https://github.com/AzureMentor/Azure-AZ-900-Study-Guide/blob/master/1-Describe%20cloud%20concepts%20(25%E2%80%9330%25).md)


##  Difficulties

I couldn't locate a neat list of the advantages for Azure, but easily found one for AWS.  I resorted to asking for a summary from ChatGPT and specifying that I wanted it expressed in laymens terms, which removed some of the sales jargon and clearly explained the concepts.

##  Results

1. **High Availability**:
   - Imagine you have a website or an application. High availability means that your website or app is almost always accessible and operational, even if there are technical issues or maintenance happening in the background. Azure ensures this by spreading your data and applications across multiple servers and data centers so that if one goes down, your services remain available.

2. **Depending on the service level agreement (SLA)**:
   - A service level agreement (SLA) is like a promise between you and Azure. It outlines how reliable their services will be and what happens if they don't meet those promises. Azure provides different levels of SLAs depending on the service you use. For example, they might guarantee that your services will be available 99.99% of the time. If they don't meet this, they might offer you credits or compensation.

3. **Scalability (Both vertically and horizontally)**:
   - Imagine your website suddenly becomes really popular, and lots of people are trying to use it at once. Scalability means your website can handle this increased demand without crashing. In Azure, you can scale your resources both vertically (by making your existing servers more powerful) and horizontally (by adding more servers). This ensures your website or app can handle more traffic as needed.
  
   - Vertical scaling
     
With vertical scaling, if you were developing an app and you needed more processing power, you could vertically scale up to add more CPUs or RAM to the virtual machine. Conversely, if you realized you had over-specified the needs, you could vertically scale down by lowering the CPU or RAM specifications.

  - Horizontal scaling
    
With horizontal scaling, if you suddenly experienced a steep jump in demand, your deployed resources could be scaled out (either automatically or manually). For example, you could add additional virtual machines or containers, scaling out. In the same manner, if there was a significant drop in demand, deployed resources could be scaled in (either automatically or manually), scaling in.

4. **Elasticity**:
   - Elasticity is like scalability but on autopilot. It means your resources automatically adjust based on demand. So, if your website suddenly gets a huge spike in visitors, Azure will automatically add more servers to handle the load. And when the traffic decreases, it will scale back down to save you money.

5. **Agility**:
   - Agility in Azure means you can quickly adapt and change your resources as your business needs evolve. If you want to launch a new feature or experiment with something, Azure makes it easy to do so without long delays or complex setup processes. This agility helps businesses stay competitive and respond to market changes faster.

6. **Geo distribution**:
   - Geo distribution means your data and services are spread across multiple locations or regions around the world. This is useful for businesses that have customers or users in different parts of the globe. With Azure, you can choose where your data is stored and make sure it's closer to your users, which can improve performance and reduce latency.

7. **Disaster recovery**:
   - Disaster recovery is like having a backup plan for your data and services in case something goes wrong. Azure offers tools and services to help you recover quickly from disasters like server failures, data breaches, or natural disasters. This ensures your business can keep running smoothly even in the face of unexpected events.
  
### Consumption Based Model

Capex and Opex refer to different types of expenditures a business incurs:

1. **Capex (Capital Expenditure)**:
   - Capex refers to investments in physical assets like buildings, machinery, or equipment that are expected to provide benefits to the business over multiple years.
   - These investments are typically recorded on the balance sheet and depreciated over time, meaning their costs are spread out over their useful life.

2. **Opex (Operational Expenditure)**:
   - Opex refers to day-to-day expenses necessary to keep a business running, such as rent, utilities, wages, and maintenance costs.
   - These expenses are recorded on the income statement and are incurred regularly to maintain business operations.

Now, regarding why moving from Capex to Opex is often seen as advantageous when transitioning to the cloud:

1. **Flexibility and Scalability**:
   - Opex-based models, such as cloud services, offer flexibility as they allow businesses to scale their resources up or down based on demand. This agility is particularly valuable in dynamic environments where demand fluctuates.

2. **Cost Predictability**:
   - Opex models often provide more predictable costs since businesses pay for what they use on a recurring basis. This contrasts with Capex, where the upfront investment might be substantial and the ongoing costs less predictable.

3. **Reduced Financial Risk**:
   - By shifting from Capex to Opex, businesses can reduce financial risk by avoiding large upfront investments. This is particularly relevant for startups and small to medium-sized enterprises (SMEs) with limited capital.

4. **Access to Latest Technology**:
   - Cloud service providers continually update and improve their offerings without additional cost to users. By utilizing Opex-based cloud services, businesses can access the latest technology without the need for expensive upgrades or replacements.

5. **Opportunity Cost**:
   - Investing in Capex ties up capital that could potentially be used for other investments or operational needs. Shifting to Opex allows businesses to allocate resources more efficiently, potentially increasing overall returns.

Overall, while both Capex and Opex have their advantages, the move to Opex, especially in the cloud computing realm, offers greater flexibility, scalability, and cost predictability, which are highly valued in today's dynamic business landscape.
