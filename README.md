<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This walkthrough outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Log into the Admin/Analyst Panel
- Set up Roles
- Create Departments
- Establish Teams
- Configure user settings
- Add Agents
- Add Users
- Define SLAs
- Create Help Topics

<h2>Log into Panel</h2>

<p>
  <img width="500" alt="Screen Shot 2024-12-09 at 11 43 26 PM" src="https://github.com/user-attachments/assets/61eeee0d-da98-44ba-a1f6-83bf8d08dcfd">

</p>
<p>
I accessed the Admin Panel at http://localhost/osTicket/scp/login.php using the credentials set during installation. This panel allows me to configure and manage the system.</p>
<br />

<h2>Set up Roles</h2>

<p>
<img width="300" alt="Role name" src="https://github.com/user-attachments/assets/47850f84-4de6-4cb5-b708-04f39350ed92">
<img width="300" alt="role permission tickets" src="https://github.com/user-attachments/assets/a5b287af-38ce-4615-ba4f-5dab41def436">
<img width="300" alt="role permission tasks" src="https://github.com/user-attachments/assets/9f071f9c-e508-49be-8571-729da598759e">
<img width="300" alt="role permission knowledge" src="https://github.com/user-attachments/assets/cfda04f9-289b-4dbe-9c10-a2d0d22135cd">
<img width="300" alt="added role success" src="https://github.com/user-attachments/assets/64b572cd-8ee0-4050-9f94-46e8ef06a278">

</p>
<p>
I navigated to Admin Panel -> Agents -> Roles and created a new role, "Supreme Admin." Here, I defined what agents can view or do within the system, grouping permissions by job function.
</p>
<br />

<h2>Create Departments</h2>

<p>
<img width="500" alt="adding department" src="https://github.com/user-attachments/assets/e36d2224-31ca-4165-a4a9-46e56aeb525a">
<img width="500" alt="Department created" src="https://github.com/user-attachments/assets/d05b4696-e654-46ad-8018-4c19c6da75dc">

</p>
<p>
I went to Admin Panel -> Agents -> Departments to set up departments like "SysAdmins." Each department was configured to manage tickets related to specific areas of responsibility.
</p>
<br />

<h2>Establish Teams</h2>

<p>
<img width="500" alt="adding team" src="https://github.com/user-attachments/assets/cb8c9c4d-bb44-426d-8cf3-2be55d42dfb9">
<img width="500" alt="Added team" src="https://github.com/user-attachments/assets/faf9042f-0221-468e-820c-adc34971ef1d">

</p>
<p>
Using Admin Panel -> Agents -> Teams, I created a team called "Online Banking" by pulling agents from different departments. Teams help improve collaboration across departmental boundaries.
</p>
<br />

<h2>Configure user settings</h2>

<p>
<img width="500" alt="configure user settings" src="https://github.com/user-attachments/assets/993cbde3-3875-41f7-ad91-1566ad7b076e">

</p>
<p>
I adjusted settings in Admin Panel -> Settings -> User Settings to control how users submit tickets. I unchecked the option for unregistered users to create tickets, requiring registration and login for ticket submissions.
</p>
<br />

<h2>Add Agents</h2>

<p>
<img width="325" alt="adding jane account" src="https://github.com/user-attachments/assets/5b8168fc-2c6c-48d2-93c0-602115c8a7e8">
<img width="325" alt="jane access" src="https://github.com/user-attachments/assets/10ba9d3a-dc67-44f8-8803-ea4396405248">
<img width="325" alt="adding jane team" src="https://github.com/user-attachments/assets/b91230c3-a57f-4c60-8d64-f4c8c2fa0666">
<img width="325" alt="adding john account" src="https://github.com/user-attachments/assets/22994543-bb44-4dd6-b86b-62d467697d4c">
<img width="325" alt="john access" src="https://github.com/user-attachments/assets/5d074226-253b-4c1c-9536-d051ea93392a">
<img width="325" alt="showing both added agents" src="https://github.com/user-attachments/assets/142feb1e-7206-48ee-921c-61da17e6e093">


</p>
<p>
I went to Admin Panel -> Agents -> Add New and created accounts for agents like Jane (SysAdmins) and John (Support). I assigned each agent to their respective department for ticket management.
</p>
<br />

<h2>Add Users</h2>

<p>
<img width="500" alt="creating user karen" src="https://github.com/user-attachments/assets/0b98f8d5-b807-4b01-977c-d95c252738ff">
<img width="500" alt="karen user created" src="https://github.com/user-attachments/assets/dfdcbd09-4c4b-49e2-9a4c-95e9b084684f">


</p>
<p>
In Agent Panel -> Users -> Add New, I created user accounts for customers like Karen and Ken. This setup allows them to submit tickets through the end-user interface at http://localhost/osTicket.
</p>
<br />

<h2>Define SLAs</h2>

<p>
<img width="325" alt="SLA A creating" src="https://github.com/user-attachments/assets/957f5415-4c24-4ead-81e7-f115f190e501">
<img width="325" alt="SLA B creating" src="https://github.com/user-attachments/assets/c06f1118-5fea-4741-b401-1e7e154a5360">
<img width="325" alt="SLA C creating" src="https://github.com/user-attachments/assets/299497a1-0c79-43d0-9db2-761130e62cfb">
<img width="325" alt="All SLA created" src="https://github.com/user-attachments/assets/8f1e17db-fce6-499a-8e0d-0a2896055d0d">

</p>
<p>
I configured SLAs in Admin Panel -> Manage -> SLA, defining response times based on urgency:
- Sev-A: 1-hour grace period, 24/7 schedule.
- Sev-B: 4-hour grace period, 24/7 schedule.
- Sev-C: 8-hour grace period, business hours only.</p>
<br />

<h2>Create Help Topics</h2>

<p>
<img width="300" alt="creating help topic 1" src="https://github.com/user-attachments/assets/c2d96878-bf22-4df9-bf6f-e69cb1e780f1">
<img width="300" alt="creating help topic 2" src="https://github.com/user-attachments/assets/bdf481c9-f5a6-4b6c-b1d1-29ce51407a1d">
<img width="300" alt="creating help topic 3" src="https://github.com/user-attachments/assets/d47e5e34-a83a-432f-831b-b8f1dda35b4a">
<img width="300" alt="creating help topic 4" src="https://github.com/user-attachments/assets/00be639a-4aa5-4bcc-9283-d5057746bffa">
<img width="300" alt="creating help topic 5" src="https://github.com/user-attachments/assets/564ca124-7f01-4721-9c5c-b7a423116540">
<img width="300" alt="all help topics created" src="https://github.com/user-attachments/assets/9a801159-35f1-4e88-9853-a30c7297804e">

</p>
<p>
I navigated to Admin Panel -> Manage -> Help Topics and set up categories like "Business Critical Outage," "Password Reset," and "Equipment Request." These help users select the appropriate category when submitting tickets, streamlining issue identification.

</p>
<br />
