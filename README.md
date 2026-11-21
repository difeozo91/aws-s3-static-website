# aws-s3-static-website
AWS S3 Static Website

# AWS Static Website Hosting with Amazon S3

## Project Overview

This project demonstrates how to host a static website using Amazon Simple Storage Service (Amazon S3).

The objective was to understand AWS object storage, static website hosting, bucket permissions, and resource-based access control through a practical implementation.

The website was developed using HTML and CSS and uploaded to an Amazon S3 bucket configured for static website hosting.

## Project Objectives

- Understand Amazon S3 and object storage.
- Create and configure an S3 bucket.
- Upload and manage website files.
- Enable static website hosting.
- Configure public access settings.
- Implement an S3 bucket policy.
- Understand AWS resource-based permissions.
- Test website accessibility through the S3 website endpoint.

## AWS Services and Technologies

| Service / Technology | Purpose |
|---|---|
| Amazon S3 | Stores and hosts website files |
| AWS IAM | Identity and access management concepts |
| S3 Bucket Policy | Controls access to website objects |
| HTML | Structures website content |
| CSS | Styles website content |
| Git | Version control |
| GitHub | Source code and project documentation |

## Architecture

The project uses Amazon S3 to store and serve static website content.

**Application Flow:**

1. A visitor accesses the S3 website endpoint.
2. Amazon S3 receives the request.
3. S3 retrieves the requested website object.
4. The browser displays the website content.

## Project Structure

```text
aws-s3-static-website/
│
├── README.md
├── website/
│   ├── index.html
│   ├── error.html
│   └── style.css
│
├── screenshots/
│
└── documentation/
    ├── architecture.md
    ├── implementation.md
    ├── security.md
    └── lessons-learned.md
```

## Implementation Steps

### 1. Create an S3 Bucket
Created a dedicated Amazon S3 bucket to store the website files.

### 2. Upload Website Files
Uploaded the HTML and CSS files to the S3 bucket.

### 3. Enable Static Website Hosting
Configured the S3 bucket for static website hosting and specified the index and error documents.

### 4. Configure Public Access
Reviewed the bucket's Block Public Access settings and configured the dedicated website bucket to allow public access.

### 5. Configure Bucket Policy
Implemented a bucket policy granting public read access to website objects using the `s3:GetObject` permission.

### 6. Test Website Accessibility
Accessed the generated S3 website endpoint and verified that the website loaded successfully.

## Security Considerations

- Used a dedicated S3 bucket for the practice website.
- Configured public access at the bucket level rather than changing account-wide settings.
- Granted only the permissions necessary for public website retrieval.
- Did not grant public upload or delete permissions.
- Avoided storing AWS credentials or sensitive information in the repository.
- Recognized that direct S3 website endpoints use HTTP rather than HTTPS.

**Note:** Public website hosting makes website objects accessible to anyone. CloudFront can be introduced in a future project to support HTTPS and improved content delivery.

## Project Screenshots

Screenshots documenting the implementation are available in the `screenshots/` directory.

- S3 bucket creation
- Uploaded website files
- Static website hosting configuration
- Public access settings
- Bucket policy
- Completed website
- GitHub repository

## What I Learned

Through this project, I gained practical experience with:

- Amazon S3 object storage.
- AWS static website hosting.
- S3 bucket configuration.
- AWS public access controls.
- JSON-based bucket policies.
- Resource-based permissions.
- Website deployment using AWS.
- Git and GitHub version control.

## Future Improvements

- Configure Amazon CloudFront for content delivery.
- Introduce HTTPS using AWS Certificate Manager.
- Explore custom domain configuration with Route 53.
- Automate infrastructure deployment using Terraform.

## Cost Considerations

This project was designed as a minimal-cost learning exercise.

No EC2 instances, databases, NAT Gateways, or CloudFront distributions were deployed.

Amazon S3 is usage-based, and applicable charges may depend on storage, requests, and data transfer.

Temporary AWS resources were removed after project completion.

## Project Status

Completed – Initial AWS Static Website Hosting Lab.
