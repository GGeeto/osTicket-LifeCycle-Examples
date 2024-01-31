![osTicket logo](https://i.imgur.com/Clzj7Xs.png)

# osTicket - Ticket Lifecycle Examples

This tutorial outlines the lifecycle of a ticket from intake to resolution within the open-source help desk ticketing system osTicket.

## Environments and Technologies Used

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

## Operating Systems Used 

- Windows 10 (21H2)

## Ticket Lifecycle Stages

- Intake
- Assignment and Communication
- Working the Issue
- Resolution

## Lifecycle Stages

<p>
    <img src="https://imgur.com/3GV5RSW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

This is a continuation of my osTicket Azure project. If you have not completed [osTicket-Post-Installation Configuration](https://github.com/GGeeto/osticket-Post-Installation-Configuration), ensure to do so before proceeding.

Navigate to the [osTicket Support Center](http://localhost/osTicket/). Enter the contact details of a user previously established in the last project. Within the osTicket Support Center, users are prompted to select a help topic; choose 'business critical outage' as previously configured. In the issue summary field, illustrate a scenario resembling a business critical outage, such as "Internet connection lost throughout all departments" or "Entire mobile banking website down." Elaborate on the details, crafting a scenario based on the chosen issue. Now based on the details you've crafted, assign  and proceed by clicking 'Create Ticket.' We'll repeat this process to generate two additional tickets, utilizing our other fabricated help topics. For the second ticket, utilize the contact information of the other user created, and for the third, either reuse one of the existing users or navigate to the agents panel on the staff page to create another. 
<p>
    <img src="https://imgur.com/duK8pA4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Now navigate to the [osTicket Login page](http://localhost/osTicket/scp/login.php) and log in with your account, not the ones previously created. You should find our three tickets listed. Click on the first one to view all the details. Depending on the scenario created, we can adjust the details to best match. In the example shown, the ticket falls under the 'Personal Computer Issues' help topic, with the reported issue being a slow computer. The status is open, which is accurate, but the priority was initially set to normal. For this scenario, we'll adjust it to a low priority ticket, considering the higher severity tickets we have. Now, let's examine the SLA-Plan. In this case, the personal computer issues help topic defaulted the SLA to Sev-B. However, the severity of this issue doesn't seem to align with Sev-B, so we'll adjust it to Sev-C, a much lower priority severity level.

As you navigate through the tickets, it's essential to tailor the severity and SLA plan of each according to their specific requirements. It's important to note that different companies uphold varying standards of SLA, making this part of the project inherently subjective. Engaging with professionals who actively utilize osTicket can offer valuable insights to better understand these nuances.

By clicking on the blue text adjacent to the details, you can seamlessly edit them, and reloading the page will display the updates under the ticket thread. Beneath the ticket thread, you'll find a 'Post Reply' sub-tab, which facilitates communication with the ticket owner. Maintaining constant communication with users is considered a best practice, particularly for tickets with prolonged resolution times. Adjacent to this is the "Post Internal Note" sub-tab, allowing agents to collaborate and communicate effectively, especially when multiple agents are involved in addressing the ticket.

<p>
    <img src="https://imgur.com/evGr3yD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Now on any of the three tickets, scroll back up to the details and click on '-Unassigned-'. The first Assignee will be your Administrator agent, which we previously created. For the other two tickets, assign them based on the department of the agent. In my example, the high-priority ticket subject reads "Internet Connection lost throughout the whole department." Between my created account under the maintenance department and my own account under the support department, this ticket would best fit in the maintenance department. As for the normal priority ticket subject, which says "Account Password Reset," it would be most appropriate under the support department.

<p>
    <img src="https://imgur.com/UJygSbi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Now, we'll log out of our current account and log in to any of the accounts assigned to those tickets. If one of your tickets is assigned to your own account, you can hold off logging out and enter that ticket directly. Navigate to the bottom and post one or a couple of replies fabricated according to the scenario. For instance, with the 'Password Reset' ticket, you can reply with "working on getting your account unlocked for you, thank you for your patience." Given the simplicity of this ticket, it can be resolved in the next reply. Here's an example of the subsequent response: "Hello Gene, your account has been unlocked and your one-time password is ******. Your next login will prompt you with a password reset. Thank you for your patience." This reply states the resolution of the ticket. Normally, we would wait for the response from the ticket owner to ensure the problem was solved, but for this project, let's imagine that's already happened. Now, change the Ticket status at the top from 'open' to 'resolved'.

Afterward, log in to other agents' accounts and post replies and resolutions to the other two tickets based on their scenarios.

This portion of the project demonstrates how users create tickets and how agents resolve them. Many of the elements presented are dependent on the organization that owns the osTicket Server, such as the Service Level Agreements, priority levels, and distribution of tickets to particular departments and agents. This project was solely for basic understanding of these processes within osTicket.

The project will conclude with a more in-depth analysis of configurations, going over parts of the site that haven't been covered yet.
