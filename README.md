# 🚀 AWS Static Website Hosting (S3 + CloudFront)

## 📌 Project Overview
This project demonstrates how to host a static website using AWS with a secure production-style architecture.

## 🏗️ Architecture
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

.
├── index.html
├── style.css
├── images.jpeg


## 🚀 How to Deploy
1. Create S3 bucket
2. Upload website files
3. Configure CloudFront distribution
4. Enable Origin Access Control (OAC)
5. Update bucket policy
6. Access via CloudFront URL

## 🔄 Cache Invalidation
CloudFront caches content at edge locations. When updates are made to the website, cache invalidation may be required to reflect changes immediately.

## 📌 Future Improvements
- Add custom domain using Route 53
- Add HTTPS with ACM
- Automate deployment using CI/CD

---

## 🙌 Author
pingjahangir