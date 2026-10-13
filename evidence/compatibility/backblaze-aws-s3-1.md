<!-- fetched 2026-10-13 from https://www.backblaze.com/docs/cloud-storage-s3-compatible-api by sweep-shape-compat.py; text extracted from the provider's own page -->

S3-Compatible API are not accessible in advanced search which breaks the dropdown selection functionality --> 
 B2 Cloud Storage 
 Business Backup 
 Personal Backup 
 API Documentation 
 Help 
 Sign in 
 Cloud Storage 
 Cloud Storage 
 Computer Backup 
 Contents x 
 About Backblaze B2 Cloud Storage 
 Get Started with the Web Console 
 Get Started with the Enterprise Web Console 
 AI & Machine Learning 
 Quickstart and Developer Guides 
 Backblaze B2 APIs: S3 Compatible, B2 Native, Partner API, Organizations API, and IAM-STS API 
 Community SDKs for the Backblaze B2 Cloud Storage API 
 Integration Guides 
 Additional Resources 
 S3-Compatible API
 10 Dec 2025 
 Print 
 Dark 
 Light 
 Contents 
 S3-Compatible API
 Updated on 10 Dec 2025 
 Print 
 Dark 
 Light 
 Article summary
 Did you find this summary helpful? 
 Thank you for your feedback
 The Backblaze B2 Cloud Storage S3-Compatible API does the same thing as the Native API —it allows you to interact with Backblaze B2 —but it follows the S3 syntax. With the S3-Compatible API , if your application is already written to use the S3 API, Backblaze B2 will just work, with minimal code changes on your end. The S3-Compatible API provides developers with the following benefits:
 You do not have to learn a new API.
 You can use your existing tools that are written to the S3 API.
 Performance will be just as good, and you’ll get all the benefits of Backblaze B2 .
 For all of the Backblaze API operations and their corresponding documentation, see API Documentation .
 Naming Restrictions
 The S3-Compatible API features slightly different restrictions on file and bucket names than the AWS S3 API. Refer to the Buckets and Files page for naming restrictions.
 Access Control Lists
 The S3-Compatible API features limited support for access control lists (ACLs). Get Object ACL and Get Bucket ACL calls will work as expected. However, object-level ACLs are not supported. For example, a Get Object ACL call returns the ACL for the bucket in which the object is contained.
 If a bucket is private, the ACL that is returned for the bucket and any files within the bucket are “private.” If a bucket is public, the ACL that is returned for the bucket and any files within the bucket are “public-read.”
 The S3-Compatible API supports the Put Bucket ACL call to change between "private" and “public-read” only. Attempting to put a different value returns an error.
 The call succeeds only when the specified ACL matches the ACL of the bucket.
 Pre-Signed URLs 
 The S3-Compatible API supports pre-signed URLs for downloading and uploading. You can generate pre-signed URLs using the AWS CLI, AWS Tools for PowerShell, s3cmd, and AWS SDKs.
 The following guides can help you configure these tools:
 AWS Command-Line Interface 
 s3cmd 
 Native API SDKs 
 S3-Compatible SDKs 
 Server-Side Encryption
 The S3-Compatible API supports server-side encryption of data before storing using either Backblaze -managed keys (SSE-B2) or using customer-managed keys (SSE-C). For more information on supported SSE options, click here .
 Get Object Tagging
 The S3-Compatible API does not fully support object tagging. Therefore, the implementation of Get Object Tagging returns a set of empty tags. This implementation is provided for compatibility with certain integrations.
 Copy Object and Tagging
 The S3-Compatible API does not fully support object tagging. The x-amz-tagging-directive header is allowed on the Copy Object API , but it will be ignored, no matter the value that you supply. Also, note that the x-amz-tagging header will be explicitly rejected if it is included on the Copy Object (or Put Object ) API calls. This implementation is provided for compatibility with certain integrations.
 Unsupported Features
 The S3-Compatible API does not currently support the following features:
 ACLs
 IAM Roles
 Object Tagging
 Website Configuration
 Browser-based uploads to pre-signed URLs using POST 
 IPv6 Support
 The S3-Compatible API now supports IPv6.
No changes to your code should be required to use IPv6 addresses with Backblaze B2 Cloud Storage and the S3-Compatible API .
 What is IPv6?
IPv6 is a version of the Internet Protocol that uses a larger address space than IPv4, its predecessor and currently the most common format for IP addresses. IPv6 addresses consist of eight groups of four hexadecimal digits with each group separated by a colon. For example: 2001:db8:1f70:999:de8:7648:3a49:6e8 In comparison, IPv4 notation consists of four groups of decimal digits with the groups separated by dots. For example: 198.51.100.1 Can I still use IPv4 addresses?
Yes. The S3-Compatible API will continue to support IPv4 addresses for the foreseeable future. Will using IPv6 incur additional costs?
No. Is IPv6 more secure than IPv4?
Requests to our APIs using IPv4 or IPv6 have equally secure connections and use the same strong TLS encryption.
However, some customers may see a performance improvement if IPv6 allows them to avoid NAT.
 Was this article helpful?
 Yes No 
 Thank you for your feedback! Our team will get back to you
 How can we improve this article?
 Your feedback
 Need more information 
 Difficult to understand 
 Inaccurate or irrelevant content 
 Missing/broken link 
 Others 
 Comment
 Comment (Optional)
 Character limit : 500
 Please enter your comment
 Email (Optional)
 Email
 Notify me about change 
 Please enter a valid email
 Cancel 
 Related articles
 Application Keys 
 How to Use Backblaze B2 S3-Compatible App Keys 
 Server-Side Encryption 
 Native API 
 How to Use S3-Compatible API Bucket Versions in Backblaze B2 
 S3-Compatible SDKs 
 How to Call the Backblaze B2 S3-Compatible API 
 How to Enable CORS with the Backblaze B2 S3-Compatible API 
 How to Enable Object Lock with the Backblaze B2 S3-Compatible API 
 What's Next
 How to Call the Backblaze B2 S3-Compatible API 
 Table of contents 
 Naming Restrictions 
 Access Control Lists 
 Pre-Signed URLs 
 Server-Side Encryption 
 Get Object Tagging 
 Copy Object and Tagging 
 Unsupported Features
