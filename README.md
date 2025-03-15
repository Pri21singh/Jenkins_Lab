# Jenkins_Lab
Jenkins with GitHub using the polling-based approach
# Configure Jenkins with GitHub
1. Install Required Plugins
Go to Jenkins → Manage Jenkins → Plugin Manager → Available Plugins, then install:
  Git Plugin
  Pipeline Plugin
  Email Extension Plugin
  GitHub Integration Plugin (optional but useful)
# Restart Jenkins after installation.

# Configure Jenkins to Access Your GitHub Repository
1. Generate a GitHub PAT (Personal Access Token)
Click Generate new token and select:
repo (for repository access)
admin:repo_hook (for webhooks)

# Generate and copy the token.
2. Add Credentials in Jenkins
Go to Jenkins → Manage Jenkins → Manage Credentials.
Click Global Credentials → Add Credentials.
Select "Username and Password":
Username: Your GitHub username.
Password: Paste the PAT token.

# Set Up Jenkins Polling Trigger
Go to Jenkins → Your Job → Configure.
In Build Triggers, select Poll SCM and set the schedule as:

# Configure Email Notifications

# Enable App Passwords in Gmail
Go to Google Account → Security → App Passwords.
Select Mail and Windows Computer.
Generate an App Password and copy it.

# Configure SMTP in Jenkins
Go to Jenkins → Manage Jenkins → Configure System.
Scroll to E-mail Notification and configure:
SMTP Server: smtp.gmail.com
Use SMTP Authentication
Username: Your Gmail address.
Password: Paste the App Password.
Use SSL:SMTP Port: 465
Reply-To Address: your gmail address

Step 4: Run and Test the Pipeline
Trigger a Build:

Go to Jenkins → Your Job → Build Now.
Jenkins will pull from GitHub, run the build, and send an email notification.
Check Email Alerts
