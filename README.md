<div align="center">

<img src="https://github.com/AnderMendoza/AnderMendoza/raw/main/assets/line-neon.gif" width="100%">
<br/><br/>

![Github Banner - osTicket Ticket Lifecycle](https://github.com/user-attachments/assets/6d1da7f1-0e10-4c99-baef-9855c11e4dc4)

<img src="https://github.com/AnderMendoza/AnderMendoza/raw/main/assets/line-neon.gif" width="100%">

</div>

# osTicket: Ticket Lifecycle - From Submission to Resolution

This guide walks you through the complete lifecycle of a help desk ticket in osTicket, from initial submission to final resolution, using the open-source ticketing system.

## Technologies and Environments

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop Connection (mstsc)
- Internet Information Services (IIS)
- osTicket

## Operating Systems

- Windows 11 Home (24H2)
- Windows 10 (21H2)

## Prerequisites

- [osTicket Installation and Prerequisites](https://github.com/mxwllslvr/osTicket-prerequisites-and-installation)
- [osTicket Post Installation Configuration](https://github.com/mxwllslvr/osTicket-post-installation-configuration)

## Ticket Lifecycle Stages

1. Ticket Submission (Intake)
2. Assignment and Communication
3. Issue Investigation
4. Resolution and Closure

---

## Lifecycle Steps

### Step 1: Resolving a System Issue

(Log into VM created in [osTicket Installation and Prerequisites](https://github.com/mxwllslvr/osTicket-prerequisites-and-installation). You will be using it for the remainder of this tutorial.)

<p>
<img width="750" alt="TL1" src="https://github.com/user-attachments/assets/5877500b-d073-4a08-a058-87692a50ad09"/>
</p>

1. **Issue Identification**: Clients reported that submitted tickets are not visible to agents. A test ticket confirmed the issue—tickets are created but not appearing in the agent view.
2. **Access Admin Portal**: Log into the osTicket Staff Control Panel at `http://localhost/osTicket/scp/login.php` using:
   - Username: `adminuser`
   - Password: `Password1`

<table>
  <tr>
    <td>
      <img width="1000" alt="TL2" src="https://github.com/user-attachments/assets/801571d3-8aca-4546-a313-04751bf29f06" />
    </td>
    <td>
      <img width="1000" alt="TL3" src="https://github.com/user-attachments/assets/d5a31a22-fcad-4f90-b42e-a125099516a5" />
    </td>
  </tr>
</table>

3. **Diagnose the Problem**: A recent osTicket update introduced a bug routing all tickets to the "Maintenance" department, ignoring configured settings.
4. **Delete Maintenance Department**:
   - In **Agent Panel**, navigate to **Agents** → **Departments**.
   - Select the "Maintenance" department, click **More** → **Delete**, and confirm by clicking **Yes, Do it!**

<table>
  <tr>
    <td>
      <img width="1000" alt="TL4" src="https://github.com/user-attachments/assets/9ae69e11-d0f7-456a-9329-4d46c25e4cc3" />
    </td>
    <td>
      <img width="1000" alt="TL5" src="https://github.com/user-attachments/assets/e04a3792-da9e-4d7f-bf26-cad8865da8b1" />
    </td>
  </tr>
</table>

**Observation**: After agents log out and back in, tickets are now visible and routing correctly, resolving the issue.









---

### Step 2: Ticket Submission (Intake)

<table>
  <tr>
    <td>
      <img width="1000" alt="TL6" src="https://github.com/user-attachments/assets/814f98a5-53d2-4961-8d43-0d85538b8342" />
    </td>
    <td>
      <img width="1000" alt="TL7" src="https://github.com/user-attachments/assets/91989873-058a-4867-8567-27115ae321f3" />
    </td>
  </tr>
</table>

1. **Access User Portal**: Open the osTicket Support Center at `http://localhost/osTicket`.
2. **Create a Ticket**:
   - Click **Open a New Ticket**.
   - Enter:
     - Email: `karen@lonpacific.com`
     - Name: Karen
     - Help Topic: Report a Problem
   - Fill in the issue summary as shown in the referenced image.
   - Click **Create Ticket**.

<p>
<img width="750" alt="TL10" src="https://github.com/user-attachments/assets/3c217d58-41b8-4032-8c8f-b6e850195156" />
</p>

**Observation**: The ticket is successfully created and ready for agent review.

---

### Step 3: Assignment and Initial Review

<table>
  <tr>
    <td>
      <img width="1000" alt="TL8" src="https://github.com/user-attachments/assets/17c89948-5d1a-4abd-a789-614bbea3a340"/>
    </td>
    <td>
      <img width="1000" alt="TL9" src="https://github.com/user-attachments/assets/9f80ba6a-8244-4d07-9a0a-241bd29b4afb"/>
    </td>
  </tr>
</table>

1. **Log in as Agent**:
   - Access the Staff Control Panel and log in as John Doe:
     - Username: `john_doe`
     - Password: `Password1`
   - Navigate to **Tickets** → **Open** to view all open tickets.
   - Locate and open Karen's ticket.

<p>
<img width="750" alt="TL11" src="https://github.com/user-attachments/assets/72211831-3c5f-4c79-a901-43f036c3dc59"/>
</p>

2. **Review Ticket Details**: The issue appears critical based on Karen's description. Assume a follow-up call confirmed its severity.
3. **Update Ticket Settings**:
   - Click **Default SLA**, select **Sev-A**, add a comment explaining the change, and click **Update**.
   - Click **Help Topic**, choose **Report a Problem / Business Critical Outage**, add a comment, and click **Update**.
   - Click **Unassigned**, assign to the **Digital Banking** team, add a comment, and click **Assign**.

<table>
  <tr>
    <td>
      <img width="1000" alt="TL13" src="https://github.com/user-attachments/assets/e4779e26-a5d6-465a-9cdd-1b00d7b168d4" />
    </td>
    <td>
      <img width="745" alt="TL14" src="https://github.com/user-attachments/assets/2a8167be-5421-49ca-be74-7199c02ed775" />
    </td>
  </tr>
</table>

<p>
<img width="750" alt="TL17" src="https://github.com/user-attachments/assets/c8061ca7-526b-4ff8-8ff1-be961b6b827f" />
</p>

**Observation**: The ticket thread logs all changes, ensuring transparency and tracking of updates.

