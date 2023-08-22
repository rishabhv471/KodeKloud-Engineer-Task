
<h1 id="project-nautilus">Project Nautilus</h1>

<h2 id="overview">Overview</h2>
<p>Project Nautilus is the Naval subdivision of the xFusionCorp Industries.
Nautilus Application helps the Naval forces to make smart procurement decisions of their manned or unmanned maritime systems while ensuring that the operational requirements are met. It also aims to provide the best-in-class operational support, improving the safety and life extension of existing machines and reducing the cost of ownership.</p>

<h2 id="current-repertoire">Current Repertoire</h2>
<ol>
  <li>Sonar Technology and Systems</li>
  <li>LUSV - Large Unmanned Surface Vehicles</li>
  <li>Autonomous Unmanned Undersea Pods</li>
  <li>Nuclear Submarines</li>
  <li>Laser Guidance Systems</li>
</ol>

<h2 id="application-architecture">Application Architecture</h2>
<p>Nautilus deployment architecture can be viewed <a href="https://www.lucidchart.com/documents/edit/58e22de2-c446-4b49-ae0f-db79a3318e97/0_0?shared=true">here</a></p>

<p>The Nautilus is a three-tier application and is deployed in the Stratos Datacenter in the North America Region.</p>

<ul>
  <li>
    <p><strong>Data Tier:</strong> The Data tier is the layer that stores data with the retrieval storage and execution methods made by the application layer. We are making use of MariaDB which is one of the most popular open source relational databases.</p>
  </li>
  <li>
    <p><strong>Application Tier:</strong> Makes use of a LAMP which is a stack of open-source software that can be used to create web applications. LAMP is an acronym that usually consists of the Linux OS, the Apache HTTP Server, a MySQL relational DBMS (like MariaDB), and PHP.</p>
  </li>
  <li>
    <p><strong>Client Tier:</strong> The application client which in this case is a web browser software that processes and displays HTML resources, issues HTTP requests for resources, and processes HTTP responses.</p>
  </li>
  <li>
    <p><strong>Load Balancer:</strong> Nginx is used for HTTP Load Balancing to distribute requests through multiple application servers.</p>
  </li>
</ul>

<h2 id="shared-services">Shared Services</h2>
<ul>
  <li><strong>Storage Filer:</strong> A NAS (Network Attached Storage) filer is used to provide reliable and stable external storage for the application tier servers.</li>
  <li><strong>SFTP Server:</strong> SFTP, which stands for SSH File Transfer Protocol is used to transfer data amongst two remote systems.</li>
  <li><strong>Backup Server:</strong> A staging backup system used for short term archival.</li>
  <li><strong>Jump Server:</strong> The intermediary host or an SSH gateway to a remote network hosting the Nautilus application.</li>
</ul>


<h2 id="infrastructure-details">Infrastructure Details</h2>

<table>
  <thead>
    <tr>
      <th style="text-align: left"><strong>Server Name</strong></th>
      <th style="text-align: left"><strong>IP</strong></th>
      <th style="text-align: left"><strong>Hostname</strong></th>
      <th style="text-align: left"><strong>User</strong></th>
      <th style="text-align: left"><strong>Password</strong></th>
      <th style="text-align: left"><strong>Purpose</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: left">stapp01</td>
      <td style="text-align: left">172.16.238.10</td>
      <td style="text-align: left">stapp01.stratos.xfusioncorp.com</td>
      <td style="text-align: left">tony</td>
      <td style="text-align: left">Ir0nM@n</td>
      <td style="text-align: left">Nautilus App 1</td>
    </tr>
    <tr>
      <td style="text-align: left">stapp02</td>
      <td style="text-align: left">172.16.238.11</td>
      <td style="text-align: left">stapp02.stratos.xfusioncorp.com</td>
      <td style="text-align: left">steve</td>
      <td style="text-align: left">Am3ric@</td>
      <td style="text-align: left">Nautilus App 2</td>
    </tr>
    <tr>
      <td style="text-align: left">stapp03</td>
      <td style="text-align: left">172.16.238.12</td>
      <td style="text-align: left">stapp03.stratos.xfusioncorp.com</td>
      <td style="text-align: left">banner</td>
      <td style="text-align: left">BigGr33n</td>
      <td style="text-align: left">Nautilus App 3</td>
    </tr>
    <tr>
      <td style="text-align: left">stlb01</td>
      <td style="text-align: left">172.16.238.14</td>
      <td style="text-align: left">stlb01.stratos.xfusioncorp.com</td>
      <td style="text-align: left">loki</td>
      <td style="text-align: left">Mischi3f</td>
      <td style="text-align: left">Nautilus HTTP LBR</td>
    </tr>
    <tr>
      <td style="text-align: left">stdb01</td>
      <td style="text-align: left">172.16.239.10</td>
      <td style="text-align: left">stdb01.stratos.xfusioncorp.com</td>
      <td style="text-align: left">peter</td>
      <td style="text-align: left">Sp!dy</td>
      <td style="text-align: left">Nautilus DB Server</td>
    </tr>
    <tr>
      <td style="text-align: left">ststor01</td>
      <td style="text-align: left">172.16.238.15</td>
      <td style="text-align: left">ststor01.stratos.xfusioncorp.com</td>
      <td style="text-align: left">natasha</td>
      <td style="text-align: left">Bl@kW</td>
      <td style="text-align: left">Nautilus Storage Server</td>
    </tr>
    <tr>
      <td style="text-align: left">stbkp01</td>
      <td style="text-align: left">172.16.238.16</td>
      <td style="text-align: left">stbkp01.stratos.xfusioncorp.com</td>
      <td style="text-align: left">clint</td>
      <td style="text-align: left">H@wk3y3</td>
      <td style="text-align: left">Nautilus Backup Server</td>
    </tr>
    <tr>
      <td style="text-align: left">stmail01</td>
      <td style="text-align: left">172.16.238.17</td>
      <td style="text-align: left">stmail01.stratos.xfusioncorp.com</td>
      <td style="text-align: left">groot</td>
      <td style="text-align: left">Gr00T123</td>
      <td style="text-align: left">Nautilus Mail Server</td>
    </tr>
    <tr>
      <td style="text-align: left">jump_host</td>
      <td style="text-align: left">Dynamic</td>
      <td style="text-align: left">jump_host.stratos.xfusioncorp.com</td>
      <td style="text-align: left">thor</td>
      <td style="text-align: left">mjolnir123</td>
      <td style="text-align: left">Jump Server to Access Stork DC</td>
    </tr>
    <tr>
      <td style="text-align: left">jenkins</td>
      <td style="text-align: left">172.16.238.19</td>
      <td style="text-align: left">jenkins.stratos.xfusioncorp.com</td>
      <td style="text-align: left">jenkins</td>
      <td style="text-align: left">j@rv!s</td>
      <td style="text-align: left">Jenkins Server for CI/CD</td>
    </tr>
  </tbody>
</table>
