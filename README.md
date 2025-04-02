# 🌍 Secure Static Website Hosting with AWS S3 and CloudFront

## Tools and Platforms Utilized
- **Frontend:** HTML5, CSS
- **Cloud Infrastructure:** AWS S3 and CloudFront
- **CI/CD:** GitHub Actions
- **Version Control:** GitHub
- **Code Management:** Visual Studio Code (VS Code)
- **Authentication & Access Control:** AWS IAM

## 📌 Project Overview 
This guide details the process of securely hosting a static website on AWS without exposing the S3 bucket to the public. The project includes automatic deployment using GitHub Actions and CloudFront for improved performance and security.

---
## 📐 Architecture Diagram
![Alt Text]([images/my-image.png](https://github.com/Trivancee/AWS-S3-Cloudfront-Hosting/blob/1047dd3864a29f6e2575967551d96573ef092949/static-website-hosting.PNG))

---

## 📂 Project Structure
```sh
S3-cloudfront/
│
├── index.html              # Main website entry point
├── styles.css              # Global styles
├── assets/                 # Static resources (images, fonts)
│
└── .github/
    └── workflows/
        └── deploy.yml      # CI/CD pipeline configuration
```
---

## 🔧 Steps to Set Up Secure Static Website Hosting

### ✅ **1. Set Up the GitHub Repository**
```sh
- Create a new GitHub repository to store your static website files.
- Clone the repository to your local machine.
- Initialize the project structure with HTML and CSS files.
```

### ✅ **2. Create the Static Website Files**
- Develop the static website using HTML5 and CSS.
- Ensure the necessary assets (images, stylesheets) are included.
- Test locally using a browser or local server.

### ✅ **3. Configure AWS S3 for Static Website Hosting**
- **(a) Configure Public Access Settings**: Block all public access.
- **(b) Enable Static Website Hosting**: Set up index.html as the default document.
- **(c) Set Up Bucket Permissions for Public Access**: Grant access only via CloudFront.

### ✅ **4. Create an IAM User and Access Keys for GitHub Actions**
- **(a) Assign Permissions**: Grant necessary permissions for deployment.
- **(b) Generate Access Keys for GitHub Actions**: Store securely.

### ✅ **5. Store AWS Credentials in GitHub Secrets**
- Add `AWS_ACCESS_KEY_ID` and `AWS_SECRET_ACCESS_KEY` to GitHub Secrets.

### ✅ **6. Configure GitHub Actions for Automatic Deployment**
- Set up a GitHub Actions workflow (`deploy.yml`) for continuous deployment.

### ✅ **7. Set Up CloudFront for Secure Distribution**
- Create a CloudFront distribution with the S3 bucket as the origin.
- Restrict direct S3 bucket access and use CloudFront for content delivery.

### ✅ **8. Automate CloudFront Cache Invalidation**
- **(a) Modify the User's IAM Policy** to allow invalidation of CloudFront caches.

### ✅ **9. Update GitHub Actions Workflow**
- Add cache invalidation commands to GitHub Actions for smooth updates.

---

## 📢 **Final Steps**
- Deploy your static website using GitHub Actions.
- Test the website via the CloudFront distribution URL.
- Monitor and optimize performance using AWS CloudWatch.

---

## 🎉 Congratulations! You have successfully:
✅ Set up an S3 bucket for secure static website hosting.
✅ Configured CloudFront for enhanced security and performance.
✅ Implemented IAM-based authentication to control access.
✅ Automated deployments using GitHub Actions.
✅ Enabled automatic cache invalidation for seamless updates.

By leveraging AWS S3 and CloudFront, this approach ensures a scalable, cost-effective, and secure way to host static websites. With automated deployments and access controls in place, your website remains efficient, up-to-date, and protected from unauthorized access.

👩‍💻 Author

Ogechi G. Egbodo

Cloud and DevOps Engineer
