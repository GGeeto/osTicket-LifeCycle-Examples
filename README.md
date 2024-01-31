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

Now navigate to the [osTicket Login page](http://localhost/osTicket/scp/login.php) and login with your account, not the ones we made. Our three tickets should be present. Click on the first one and you will see all the details of the ticket. Depending on the scenario created we can change the details to best match. My example in the image shows an ticket under the 'Personal Computer Issues' help topic. Here we can see the issue is their computer running slowly. The status is open which is correct but the priority was default set to normal. For this scenerio we are going to set it low priority ticket considering the higher severity tickets we have. Now we're going to look at the SLA-Plan. In this example the personal computer issues help topic defaulted the SLA to Sev-B. But this issue does not seem to match the severity level so we are going to set this to Sev-C a much lower priority severity level.


Now on your end, go through all three tickets made and better fit the severity and SLA plan of each of them. Keep in mind that different companies have different standards of SLA, so this part of the project is completely subjective and talking to proffessionals who actively use osTicket could help you get a better idea. Clicking on the blue text next to the details will allow you to edit them and reloading the page show you the updates made under the ticket thread. Under the Ticket thread you can see a 'Post Reply' sub-tab you can use for communication with the ticket owner. Constant communication with the users is the best practice especially if it's a ticket with a prolounged resoloution time. Right next to that is the "Post Internal Note' sub-tab which allows agents to communicate with eachother if multiple of them are working on the ticket.

<p>
    <img src="https://imgur.com/evGr3yD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Now on any of the three tickets scroll back up to the details and click on '-Unassigned-'. The first Assignee is going to be your Administrator agent we created. The other two tickets can be assigned based on the department of the agent. In my exmaple my high priority ticket subject says "Internet Connection lost throughout the whole department". Between my created account under the matinence department and my own account under the support department. This ticket would best fit in the matinence department. And my normal priority ticket subject says "Account Password Reset" which would best fit under the support department. 

<p>
    <img src="https://imgur.com/UJygSbi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Now we are going to login out of our own account and login to any of the accounts assigned to those tickets. If one of your tickets is assigned to your own account you can hold on logging out and enter that ticket. Navigate to the bottom and post one or a couple of replies fabricated according to the scenario. For example my 'Password Reset' ticket I can reply with "working on getting your account unlocked for you, thank you for your patience". With how simplisitc this ticket is I can resolve it in the next reply. My next response goes as follows, "Hello Gene, your account has been unlocked and your one-time password is ******. Your next login will prompt you with a password reset, thank you for your patience.". This reply states the resolution of the ticket, and normally we would wait for the response from the ticket owner to ensure the problem was solved but for this project we are going to imagine that happened already. Now we can change the Ticket status at the top from 'open' to 'resolved'. Now we can login to our other agents accounts and post replies and resolutions to the other two tickets based on their scenarios.

This Portion of the project demonstrated how users create tickets and how agents resolve those tickets. Many of the elements presented are dependent on the organization that owns the osTicket Server. Such as the Service Level agreements, priority levels, distribution of tickets to particular departments and agents. This project was soley for basic understanding of these processes and how to do so withtin osTicket. 

This project will conclude with more in depth analysis of configurations going over parts of the site that haven't been covered yet.
