# 🚀 End-to-End DevOps Automation WebApp

A simple static web application demonstrating an end-to-end **DevOps CI/CD pipeline** using GitHub, GitHub Actions, Slack ChatOps, and Netlify.

This project was developed as part of a Virtual Lab experiment to demonstrate automation, continuous integration, continuous deployment, version control, ChatOps, and cloud-based static hosting.

---

## 📌 Project Overview

The objective of this project is to automate the complete software delivery workflow.

Whenever a developer pushes changes to the GitHub repository:

1. GitHub receives the code changes.
2. GitHub Actions automatically starts the CI pipeline.
3. The application files are verified.
4. Build and test steps are executed.
5. Slack receives a CI status notification.
6. Netlify automatically deploys the latest version.
7. The updated website becomes available through a live production URL.

---

## 🏗️ Architecture

```text
                 👨‍💻 Developer
                      |
                      | git push
                      ↓
              ┌───────────────┐
              │    GitHub     │
              │  Repository   │
              └───────┬───────┘
                      |
                      ↓
             ┌─────────────────┐
             │ GitHub Actions  │
             │                 │
             │ Checkout        │
             │ Build           │
             │ Test            │
             │ Generate Logs   │
             └───────┬─────────┘
                     |
              ┌──────┴──────┐
              ↓             ↓
        ┌──────────┐   ┌───────────┐
        │  Slack   │   │  Netlify  │
        │ ChatOps  │   │    CD     │
        └──────────┘   └─────┬─────┘
                             |
                             ↓
                     🌐 Live Website
🎯 Aim

To develop, automate, monitor, and deploy a web application using:

Git-based CI/CD
GitHub Actions
Slack ChatOps
Static cloud deployment
Netlify
Git version control
🧰 Technologies Used
Category	Technology
Frontend	HTML5
Styling	CSS3
Version Control	Git
Repository	GitHub
CI/CD	GitHub Actions
ChatOps	Slack
Cloud Deployment	Netlify
Code Editor	Visual Studio Code
Operating System	Windows
📁 Project Structure
devops-webapp/
│
├── .github/
│   └── workflows/
│       └── ci.yml
│
├── index.html
├── style.css
└── README.md
🔄 CI/CD Workflow
1. Development

The developer modifies the application locally using Visual Studio Code.

2. Version Control

Changes are committed using Git:

git add .
git commit -m "Update website"
git push origin main
3. Continuous Integration

A push to the main branch automatically triggers GitHub Actions.

The CI pipeline performs:

Source code checkout
HTML file verification
CSS file verification
Build process
Test process
Log generation
4. ChatOps

After the CI pipeline finishes, Slack receives a notification.

Successful build:

✅ CI Pipeline SUCCESS - devops-webapp

Failed build:

❌ CI Pipeline FAILED - devops-webapp
5. Continuous Deployment

Netlify is connected to the GitHub repository.

Whenever a new commit is pushed to main, Netlify automatically deploys the updated website.

⚙️ GitHub Actions Pipeline

The CI workflow is stored at:

.github/workflows/ci.yml

The workflow performs the following operations:

Checkout Code
      ↓
Verify HTML File
      ↓
Verify CSS File
      ↓
Build
      ↓
Test
      ↓
Generate Logs
      ↓
Slack Notification
💬 Slack ChatOps

Slack is integrated with GitHub Actions using an Incoming Webhook.

A GitHub repository secret is used to securely store the webhook:

SLACK_WEBHOOK_URL

The webhook URL is not stored directly in the source code.

Slack notifications provide immediate information about the CI pipeline status.

☁️ Netlify Deployment

The project is deployed using Netlify.

Deployment configuration:

Repository: devops-webapp
Branch: main
Build Command: None
Publish Directory: .

Netlify automatically publishes new commits from the GitHub repository.

🌐 Live Website

Add your Netlify production URL here:

https://snazzy-fenglisu-28c640.netlify.app/
🧪 Testing the Pipeline

To test the complete DevOps workflow:

Modify index.html.
Save the changes.
Commit the changes.
Push them to GitHub.

Example:

git add .
git commit -m "Test automatic deployment"
git push origin main

The following sequence occurs automatically:

Git Push
   ↓
GitHub Actions
   ↓
Build & Test
   ↓
Slack Notification
   ↓
Netlify Deployment
   ↓
Updated Live Website
📊 Expected Results

The project successfully demonstrates:

✅ Git-based version control
✅ Automated CI pipeline
✅ Automated build process
✅ Automated testing
✅ Build log generation
✅ Slack ChatOps notifications
✅ Automatic cloud deployment
✅ Static website hosting
✅ Continuous deployment
📸 Experiment Evidence

The following screenshots can be included in the experiment report:

1. GitHub Repository

Shows the project source code and repository.

2. GitHub Actions

Shows a successful CI pipeline execution.

3. Slack ChatOps

Shows the automated CI success notification.

4. Netlify Deployment

Shows the successful production deployment.

5. Live Website

Shows the deployed web application with its production URL.

🎓 Learning Outcomes

After completing this project, the following DevOps concepts were demonstrated:

Continuous Integration (CI)
Continuous Deployment (CD)
Git workflows
GitHub Actions
Automated testing
Build automation
ChatOps
Webhooks
GitHub Secrets
Cloud-based static hosting
Automated deployments
DevOps collaboration practices
🔐 Security

Sensitive credentials are not stored directly in the source code.

The Slack webhook is stored using GitHub Repository Secrets:

SLACK_WEBHOOK_URL

This prevents the webhook URL from being exposed in the public repository.

🚀 Future Enhancements

Possible improvements include:

Add automated HTML/CSS linting
Add unit tests
Add a React frontend
Add deployment status notifications
Add Slack failure alerts
Add pull-request based CI workflows
Add code quality analysis
Add security scanning
Add custom domain configuration
Add monitoring and analytics
📝 Conclusion

This project successfully demonstrates an end-to-end DevOps automation workflow.

The application uses GitHub for version control, GitHub Actions for Continuous Integration, Slack for ChatOps notifications, and Netlify for Continuous Deployment and static cloud hosting.

The automated workflow reduces manual deployment effort and provides immediate build status notifications, demonstrating how modern DevOps practices can be applied to a real-world web application.

👨‍💻 Author

Sashwath

GitHub:
https://github.com/sas1zzz

⭐ Project Status
🟢 CI Pipeline       : Working
🟢 Slack ChatOps     : Working
🟢 Netlify CD        : Working
🟢 Static Hosting    : Working
🟢 End-to-End Flow   : Completed