---
layout: default
title: What is LASER?
parent: LASER Info
nav_order: 1
---

## Leeds Analytic Secure Environment for Research 

### Technical controls and services based on risk  
<table class="tg">
<thead>
  <tr>
    <th></th>
    <th>Tier 3</th>
    <th>Tier 4</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td colspan=3; style="text-align: center">Technical Controls</td>
  </tr>
  <tr>
    <td style="text-align: center">User Device</td>
    <td style="text-align: center">Managed</td>
    <td style="text-align: center">Thin client / Managed</td>
  </tr>
  <tr>
    <td style="text-align: center">Authentication</td>
    <td style="text-align: center"; colspan=2>Dual (MFA)</td>
  </tr>
    <tr>
    <td style="text-align: center">Software</td>
    <td style="text-align: center"; colspan=2>Managed</td>
  </tr>
  <tr>
    <td style="text-align: center">Data Transfer</td>
    <td style="text-align: center">PI (or delegate)</td>
    <td style="text-align: center">DAT</td>
  </tr>
  <tr>
    <td style="text-align: center">Limitation</td>
    <td style="text-align: center"; colspan=2>No copy/paste, No email, No print, No local save, No internet access</td>
  </tr>
  <tr>
    <td style="text-align: center">Network Protection</td>
    <td style="text-align: center"; colspan=2>Project-level isolated network</td>
  </tr>
    <tr>
    <td style="text-align: center">Encryption</td>
    <td style="text-align: center"; colspan=2>At rest and in transit</td>
  </tr>
    <tr>
    <td style="text-align: center"; colspan=3>Physical Controls</td>
  </tr>
    <tr>
    <td style="text-align: center">Access Point</td>
    <td style="text-align: center">Shared secure office</td>
    <td style="text-align: center">Project safe room or enhanced shared secure office</td>
  </tr>
    <tr>
    <td style="text-align: center"></td>
    <td style="text-align: center"></td>
    <td style="text-align: center"></td>
  </tr>
</tbody>
</table>

![image](https://user-images.githubusercontent.com/25124181/119112449-00c9ae00-ba1c-11eb-81a9-d6d890570bcc.png)

LASER offers the combination of meeting the highest standards of security for data analytics, of course ensuring ISO27001 and NHS Data Security and Protection Toolkit compliance with the fexibility to enable constant agility in design and function; alongside scalability depending on the researcher need. This platform is supported through a commitment backed up by both LIDA and the University of Leeds IT Service to ensure high quality service wrap around to maximise ease and efficiency of time for researchers.

### What is a Virtual Research Environment? 
LASER is the platform upon which we can build and host Virtual Research Environments (VREs). 

In their simplest form, a VRE is a virtualised environment consisting of virtual machines and shared storage where data flow is strictly controlled. Taking a 'walled garden' approach, there is _no access to the internet_ or other networks from inside a VRE. 

Research is conducted by connecting to a virtual machine (VM) within a VRE. The VMs within a single VRE can all see the same project shared storage, which is inaccessible from other VREs. Software can be installed to and run directly on the VMs. 

![LASER.png](../../images/index/laser_smol.png)

More complex and involved VREs can be designed; please discuss your project requirements with a member of the Data Analytics Team as early as possible to explore what might be suitable.

**The LASER Platform has been designed with and for researchers and includes the following capabilities:**
- Fully flexible and scalable to enable researchers to align spend to research requirements.
- Agile and quick to provision, to support a range of research user cases.
- Access to the latest tools and capabilities such as machine learning to support researchers. 

### Standards & Specifications
**The system has been specified and is maintained to ensure the highest standards of data security:**
- Resilience levels and backups provided by one of the most cyber-aware and heavily invested companies in the world. 
- Regularly patched with the latest software and operating system updates.
- Encryption at rest – all data at rest is encrypted to AES256 Bit encryption.
- Encryption in transit – all data is encrypted using TLS 1.2.
- Residency – all data is stored in the UK.
- Access Controls – role-based access controls and the principles of least privileged access are implemented to ensure only authorised users are able to view data.
- Data are classified according to sensitivity and criticality, with robust checks on data input and output to and from the Cloud, including a fully maintained asset register.
- Multifactor authentication is implemented with the ability to restrict access to specified safe rooms on Campus, for data requiring the highest level of security.
- Monitoring and threat detection provides unified security management with supporting network controls to isolate information in our networks and its supporting information processing facilities.
- ISO27001 compliant.
- NHS Data Security and Protection Toolkit compliant. 

If you have any questions or are interested in working with LIDA and using the LASER platform, please contact a member of the [Data Analytics Team](mailto:ircdst@leeds.ac.uk)
