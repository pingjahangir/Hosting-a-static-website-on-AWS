# 🚀 AWS Static Website Hosting (S3 + CloudFront)

## 📌 Project Overview
This project demonstrates how to host a static website using AWS with a secure production-style architecture.

## 🏗️ [Architecture](images.jpeg/architecture.jpg)
user --> CloudFront --> S3

## 🔧 Services Used
- Amazon S3 (storage & static hosting)
- Amazon CloudFront (CDN)
- S3 Bucket Policy (IAM-based access control)
- CloudFront Origin Access Control (OAC)

## 🔐 Security Implementation
- S3 bucket is **private**
- Access restricted using CloudFront Origin Access Control (OAC)
- Direct S3 access is blocked

## ⚡ Key Learnings
- How static website hosting works in AWS
- Difference between public and private S3 buckets
- CDN (CloudFront) and caching (cache hit vs miss)
- How to secure S3 using CloudFront

## ⚠️ Challenges Faced
- Access Denied errors due to incorrect bucket policy
- Understanding difference between S3 website endpoint vs bucket endpoint
- Fixing encoding issue (UTF-8 for emoji display)

## 🌐 Live Demo
https://d35zaqpdef03k4.cloudfront.net/

## 📁 Project Structure

1. [index.html](index.html)
2. [style.css](style.css)
3. [images.jpeg](images.jpeg)
4. [policy](policy)

## 🚀 How to Deploy
1. Create S3 bucket
2. Upload website files
3. Configure CloudFront distribution
4. Enable Origin Access Control (OAC)
5. Update bucket policy
6. Access via CloudFront URL

## 🛠️ Steps to Follow
1. Create a simple website
- [index.html](index.html)
- [style.css](style.css)
2. S3 Setup
- Create S3 bucket
- Enable static website hosting
- Upload files
3. Make Website Public
- Do it by making a bucket policy [policy](policy/public_bucket.txt)
4. Access the *LIVE* Website 
* http://your-bucket-name.s3-website-region.amazonaws.com (your link must be looking like this)
* make sure to turn OFF the Block Public Access setting.
5. Add CloudFront
* Create CloudFront distribution
* Set origin = S3 bucket
* Enable caching
* To make the S3 secure again from public to private turn back ON Block Public Access setting and Change the public policy by this [policy](policy/private_bucket.txt)
* this enables the [OAC](images.jpeg/CloudFront_origin.jpg) (Origin Access Control)
* You will end-up with a secure CDN CloudFront URL like : https://dxxxxx.cloudfront.net to access your website.


**Now you have put a global Caching layer infront of S3 and turned it into a secure production grade delivery system**

## 🔄 Cache Invalidation
CloudFront caches content at edge locations. When updates are made to the website, cache invalidation may be required to reflect changes immediately.

## 📌 Future Improvements
- Add custom domain using Route 53
- Add HTTPS with ACM
- Automate deployment using CI/CD

---

## Author
pingjahangir