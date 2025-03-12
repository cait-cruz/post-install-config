<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>



<h1>Post-Installation Configuration of osTicket</h1>
<p>This tutorial outlines the <strong>post-installation configuration</strong> of <strong>osTicket</strong>, an open-source help desk ticketing system. These steps ensure proper user roles, ticket visibility, agent assignments, and service level agreements (SLAs) for effective ticket management.</p>
<hr>

<h2>Environments & Technologies Used</h2>
<ul>
    <li><strong>osTicket</strong> – Open-source help desk ticketing system</li>
    <li><strong>Apache/IIS Web Server</strong> – Hosts the osTicket application</li>
    <li><strong>PHP</strong> – Required for running osTicket</li>
    <li><strong>MySQL</strong> – Database management system for storing ticket information</li>
    <li><strong>HeidiSQL</strong> – Database administration tool</li>
    <li><strong>Remote Desktop Protocol (RDP)</strong> – Used to access the virtual machine (if applicable)</li>
</ul>

<h2>Operating Systems Used</h2>
<ul>
    <li><strong>Windows 10</strong> (or Windows Server for production environments)</li>
</ul>

<h2>Objectives</h2>
<ul>
    <li>Understand the difference between the <strong>Admin Panel</strong> and <strong>Agent Panel</strong>.</li>
    <li>Set up <strong>Roles</strong> to define agent permissions.</li>
    <li>Configure <strong>Departments</strong> for ticket visibility and routing.</li>
    <li>Organize <strong>Teams</strong> to group agents across departments.</li>
    <li>Adjust <strong>Ticket Creation Settings</strong> to allow or restrict unregistered users from submitting tickets.</li>
    <li>Add <strong>Agents</strong> (help desk staff) and <strong>Users</strong> (customers).</li>
    <li>Set up <strong>SLA Policies</strong> to manage response times for different priority levels.</li>
    <li>Define <strong>Help Topics</strong> for efficient ticket categorization.</li>
</ul>

<hr>

<h2>Post-Installation Configuration</h2>
<ul>
    
<h3>1. Access osTicket</h3>
<ul>
    <li><strong>Admin/Analyst Login Page:</strong> <a href="http://localhost/osTicket/scp/login.php">http://localhost/osTicket/scp/login.php</a></li>
    <li><strong>End User Portal:</strong> <a href="http://localhost/osTicket">http://localhost/osTicket</a></li>
</ul>

<h3>2. Understand the Agent Panel vs. Admin Panel</h3>
<ul>
    <li><strong>Admin Panel:</strong> Used for system-wide configurations, including agents, roles, departments, and SLAs.</li>
    <li><strong>Agent Panel:</strong> Used by support staff to manage and respond to tickets.</li>
</ul>

<h3>3. Configure Roles (Permissions for Agents)</h3>
<p>Navigate to <strong>Admin Panel → Agents → Roles</strong> to define roles based on access levels.</p>
<ul>
    <li><strong>Example Role:</strong> <em>Supreme Admin</em> – Grants full administrative privileges.</li>
</ul>
<br />

![image](https://github.com/user-attachments/assets/ca01c8fb-5aa2-42a1-b4c6-9432fe2024b6)

![image](https://github.com/user-attachments/assets/a7f8ce3c-c0ff-4148-88d7-1588eee670c4)


<h3>4. Configure Departments (Ticket Visibility & Routing)</h3>
<p>Navigate to <strong>Admin Panel → Agents → Departments</strong> to create departments based on ticket categories.</p>
<ul>
    <li><strong>SysAdmins</strong> – Handles IT infrastructure and system issues.</li>
    <li><strong>Help Desk</strong> – Provides general IT support.</li>
    <li><strong>Networking</strong> – Manages network-related issues.</li>
</ul>
<br />

![image](https://github.com/user-attachments/assets/2dfb5ed1-fa4f-4b70-b359-f4cd75702f8a)


<h3>5. Configure Teams (Cross-Department Collaboration)</h3>
<p>Navigate to <strong>Admin Panel → Agents → Teams</strong> to group agents across different departments.</p>
<ul>
    <li><strong>Example Team:</strong> <em>Online Banking</em> – Consists of agents from multiple departments to handle online banking support.</li>
</ul>
<br />

![image](https://github.com/user-attachments/assets/b3c184cb-4411-45bc-b5d7-9a7d4dffb842)


<h3>6. Allow or Restrict Ticket Creation</h3>
<p>Navigate to <strong>Admin Panel → Settings → User Settings</strong> to control ticket submission rules.</p>
<ul>
    <li><strong>To allow anyone to create tickets:</strong> <em>UNCHECK</em> "Require registration and login to create tickets."</li>
    <li><strong>To require user registration before ticket creation:</strong> <em>CHECK</em> "Require registration and login to create tickets."</li>
</ul>
<br />

![image](https://github.com/user-attachments/assets/ff575b13-0342-4d16-81ae-f1190012a8ff)


<h3>7. Configure Agents (Help Desk Staff)</h3>
<p>Navigate to <strong>Admin Panel → Agents → Add New</strong> to add support agents. Configure their <strong>Access, Permissions, and Teams</strong> where applicable.</p>
<ul>
    <li><strong>Example:</strong> Jane – Assigned to <em>SysAdmins</em>.</li>
    <li><strong>Example:</strong> John – Assigned to <em>Support</em>.</li>
</ul>
</br>

![image](https://github.com/user-attachments/assets/fae4e636-adae-4f86-a730-d59455995f9c)

![image](https://github.com/user-attachments/assets/552b70c3-088b-44a5-8df8-ba330e2f4bc1)

![image](https://github.com/user-attachments/assets/ddb8c429-2fcd-453a-8195-dde4f0d5d34f)



<h3>8. Configure Users (End Customers)</h3>
<p>Navigate to <strong>Agent Panel → Users → Add New</strong> to register users who will submit tickets.</p>
<ul>
    <li><strong>Example:</strong> Karen</li>
    <li><strong>Example:</strong> Ken</li>
</ul>
<br/>

![image](https://github.com/user-attachments/assets/d9a1b557-0232-43f5-a266-09a3ea7b124b)

![image](https://github.com/user-attachments/assets/89199c0a-5384-428a-a084-28784f4dc8db)

<h3>9. Configure SLA (Service Level Agreements)</h3>
<p>Navigate to <strong>Admin Panel → Manage → SLA</strong> to define ticket response times based on priority.</p>
<ul>
    <li><strong>Sev-A:</strong> 1-hour grace period, 24/7 support.</li>
    <li><strong>Sev-B:</strong> 4-hour grace period, 24/7 support.</li>
    <li><strong>Sev-C:</strong> 8-hour grace period, Business Hours only.</li>
</ul>
<br />

![image](https://github.com/user-attachments/assets/27bfed4d-b247-45fe-aa1e-94fac59fb76a)

<h3>10. Configure Help Topics (Ticket Categories)</h3>
<p>Navigate to <strong>Admin Panel → Manage → Help Topics</strong> to create predefined ticket categories.</p>
<ul>
    <li>Business Critical Outage</li>
    <li>Personal Computer Issues</li>
    <li>Equipment Request</li>
    <li>Password Reset</li>
    <li>Other</li>
</ul>
<br />

![image](https://github.com/user-attachments/assets/75a55e8f-f1eb-47e6-b58b-051a0f95e98e)
<br />
<br />
<hr>

<h3>🎉 Congratulations! osTicket is now fully configured and ready for use. 🎉</h3>

</body>
</html>

