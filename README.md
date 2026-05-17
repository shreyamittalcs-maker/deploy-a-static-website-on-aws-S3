# Task 1 - Deploy a Static Website on AWS S3

## Objective
The primary goal of this task was to host a static website using Amazon S3 (Simple Storage Service) and make it publicly accessible through a unique URL.

---

# Services Used
- AWS S3
- Static Website Hosting

---

# Project Files
The website contains:
- index.html
- style.css
- script.js
- images folder

---

# Step 1: Creating the S3 Bucket

1. Logged into the AWS Management Console
2. Navigated to the S3 service
3. Clicked on **Create Bucket**
4. Entered a unique bucket name:
   ```bash
   my-cloud-project03
   ```
5. Selected the AWS Region
6. Disabled **Block Public Access** settings
7. Created the bucket successfully

---

# Step 2: Uploading Website Files

Uploaded the following files into the S3 bucket:
- index.html
- style.css
- script.js
- images folder

All files were uploaded successfully.

---

# Step 3: Enabling Static Website Hosting

1. Opened the bucket
2. Navigated to the **Properties** tab
3. Scrolled to **Static Website Hosting**
4. Clicked **Edit**
5. Enabled Static Website Hosting
6. Added:
   ```bash
   index.html
   ```
   as the index document
7. Saved changes

AWS generated a Bucket Website Endpoint URL.

---

# Step 4: Configuring Bucket Policy

Added a bucket policy to allow public read access.

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::my-cloud-project03/*"
    }
  ]
}
```

---

# Step 5: Testing the Website

1. Copied the Bucket Website Endpoint
2. Opened the URL in the browser
3. Verified that the website was accessible publicly

---

# Live Website Link

http://my-cloud-project03.s3-website-ap-southeast-2.amazonaws.com

---

# Status

✅ Task Completed Successfully

---

# Learning Outcomes

Through this task, I learned:
- Basics of AWS S3
- Static website hosting
- Bucket permissions and policies
- Public access configuration
- Cloud-based website deployment

---

# Author

Shreya Mittal
```
