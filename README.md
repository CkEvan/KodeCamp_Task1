# KodeCamp_Task1
## How to Set up Infrastructural Structure of a Small business
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DevOps Task Solution</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
        }
        h1, h2 {
            color: #333;
        }
        pre {
            background-color: #f4f4f4;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
            }
    </style>
</head>
<body>

<h1>TASK</h1>
<p>As a DevOps Engineer, you have been consulted to set up the infrastructure servers of a small business. Create users, and assign them to groups. Create the Company directories and assign the right access to the right groups.</p>

<h1>SOLUTION</h1>

<h2>Setting Up the Environment and User Accounts</h2>

<ol>
    <li><strong>Spin up the virtual environment:</strong>
        <p>Navigate to the project directory and use the command:</p>
        <pre><code>vagrant up</code></pre>
    </li>
    <li><strong>Create a user account for the DevOps Engineer:</strong>
        <p>Use the following command to create a user named Chika with the comment "DevOps Engineer":</p>
        <pre><code>sudo adduser -c "DevOps Engineer" chika</code></pre>
    </li>
    <li><strong>Assign a password to the user Chika:</strong>
        <pre><code>sudo passwd chika</code></pre>
    </li>
    <li><strong>Grant sudo privileges to Chika:</strong>
        <pre><code>sudo usermod -aG sudo chika</code></pre>
    </li>
    <li><strong>Log into Chika's account:</strong>
        <pre><code>su chika</code></pre>
    </li>
</ol>

<h2>User and Group Management</h2>

<ol>
    <li><strong>Create users and assign comments:</strong>
        <pre><code>sudo useradd -c "System Administrator" andrew
sudo useradd -c "Legal" julius
sudo useradd -c "Human Resource Manager" chizi
sudo useradd -c "Sales Manager" jeniffer
sudo useradd -c "Business Strategist" adeola
sudo useradd -c "CEO" bach
sudo useradd -c "IT intern" gozie
sudo useradd -c "Finance Manager" ogochukwu</code></pre>
    </li>
    <li><strong>Assign passwords to each user:</strong>
        <pre><code>sudo passwd andrew
sudo passwd julius
sudo passwd chizi
sudo passwd jeniffer
sudo passwd adeola
sudo passwd bach
sudo passwd gozie
sudo passwd ogochukwu</code></pre>
    </li>
    <li><strong>Create groups and add users to appropriate groups:</strong>
        <pre><code>sudo groupadd IT_Team
sudo usermod -aG IT_Team gozie
sudo usermod -aG IT_Team andrew

sudo groupadd Legal_Team
sudo usermod -aG Legal_Team julius

sudo groupadd Sales_Team
sudo usermod -aG Sales_Team jeniffer

sudo groupadd HR
sudo usermod -aG HR chizi

sudo groupadd Business_Team
sudo usermod -aG Business_Team adeola

sudo groupadd Finance_Team
sudo usermod -aG Finance_Team ogochukwu</code></pre>
    </li>
    <li><strong>Confirm user and group creation:</strong>
        <pre><code>cat /etc/passwd
cat /etc/group</code></pre>
    </li>
</ol>

<h2>Creating Directories for Kode Camp Stores Architecture</h2>

<ol>
    <li><strong>Create the main directory and subdirectories:</strong>
        <pre><code>mkdir KodeCamp_Scores
cd KodeCamp_Scores

mkdir Finance_Budgets
mkdir Contract_Documents
mkdir Business_Projections
mkdir Business_Models
mkdir Employee_Data
mkdir CompanyVision_MissionStatement
mkdir Server_Configuration.Script</code></pre>
    </li>
</ol>

<h2>Assigning Directory Permissions</h2>

<ol>
    <li><strong>Assign group ownership to directories:</strong>
        <pre><code>sudo chown -R :Finance_Team ./Finance_Budgets
sudo chown -R :Legal_Team ./Contract_Documents
sudo chown -R :Sales_Team ./Business_Projections
sudo chown -R :Business_Team ./Business_Models
sudo chown -R :HR ./Employee_Data
sudo chown -R :HR ./CompanyVision_MissionStatement
sudo chown -R :IT_Team ./Server_Configuration.Script</code></pre>
    </li>
    <li><strong>Verify directory permissions:</strong>
        <pre><code>ls -ld Finance_Budgets/</code></pre>
    </li>
</ol>

<h2>Implementing Sticky Bits</h2>

<ol>
    <li><strong>Apply sticky bit to each directory to prevent users from deleting each other's files:</strong>
        <pre><code>sudo chmod +t ./Server_Configuration.Script/
sudo chmod +t ./CompanyVision_MissionStatement/
sudo chmod +t ./Employee_Data/
sudo chmod +t ./Business_Models/
sudo chmod +t ./Business_Projections/
sudo chmod +t ./Contract_Documents/
sudo chmod +t ./Finance_Budgets/</code></pre>
    </li>
    <li><strong>Verify the sticky bit setting:</strong>
        <pre><code>ls -ld ./Server_Configuration.Script/</code></pre>
    </li>
</ol>

<p>Following these steps, I could set up the environment, create users, assign them to groups, create necessary directories, assign permissions, and ensure directory security with sticky bits.</p>

<h2>Screenshots</h2>
<p>Below are the screenshots from my device history after completing the task:</p>

<!-- Example of including screenshots -->
<![Screenshot 2024-06-01 003106](https://github.com/CkEvan/KodeCamp_Task1/assets/154507786/a441108c-90af-489d-97cb-191a1b38c57f)>
<![Screenshot 2024-06-01 003132](https://github.com/CkEvan/KodeCamp_Task1/assets/154507786/efa05cf1-834e-427e-b021-f8e2364dbd02)
>
<![Screenshot 2024-06-01 003147](https://github.com/CkEvan/KodeCamp_Task1/assets/154507786/bfe06f47-9899-4e93-aa0d-db6b7c5d56b0)

[KodeKamp.docx](https://github.com/user-attachments/files/15519727/KodeKamp.docx) 

</body>
</html>
