---
title: "The Changing Landscape of Cloud Sync, and What It Means for Your Backup"
url: "https://www.backblaze.com/blog/the-changing-landscape-of-cloud-sync-and-what-it-means-for-your-backup/"
date: "Fri, 17 Apr 2026 23:23:38 +0000"
author: "Natasha Rabinov"
feed_url: "https://www.backblaze.com/blog/feed/"
---
<figure class="wp-block-image size-full"><img alt="An image of the Backblaze logo on a gradient background. " class="wp-image-112936" height="820" src="https://backblaze.com/blog/wp-content/uploads/2026/04/Generic-Product-updates-Blog-Header-1440x820-2-1.png" width="1440" /></figure>



<div class="wp-block-spacer" style="height: 15px;"></div>



<p>Backblaze Computer Backup was built on a simple promise: unlimited backup for everything on your computer. That promise hasn&#8217;t changed. But the way files live on your computer has, and we want to explain what&#8217;s happening, why it matters, and where we&#8217;re headed.</p>



<h2 class="wp-block-heading">How cloud sync used to work</h2>



<p>Not long ago, when you installed Dropbox or OneDrive, those apps copied your files directly onto your hard drive. They were real, local files. Backblaze would find them, back them up, and you could restore them just like anything else on your machine.&nbsp;</p>



<h2 class="wp-block-heading">What changed</h2>



<p>Over the past several years, cloud sync providers have fundamentally rearchitected how they store files at the operating system level. On Windows, tools like Dropbox and OneDrive now use something called the Cloud Files API, which represents your synced files as <a href="https://en.wikipedia.org/wiki/NTFS_reparse_point" rel="noreferrer noopener" target="_blank">reparse points</a>—essentially placeholders that point back to the cloud rather than storing actual data locally. The file appears to be there, but it&#8217;s really a redirect.</p>



<p>This isn&#8217;t a bad thing for those apps: it lets them sync efficiently and save local disk space. But it creates a real problem for backup software.</p>



<h2 class="wp-block-heading">Why we can&#8217;t reliably back up placeholders</h2>



<p>When Backblaze Computer Backup encounters a reparse point, we&#8217;re not looking at your file—we&#8217;re looking at a pointer. Backing that up wouldn&#8217;t actually protect your data; it would just save the redirect. And restoring a redirect isn&#8217;t a real restore. Since reliable backup and restore is the entire point, we made the decision to exclude folders managed this way rather than give customers a false sense of security.</p>



<p>This is also consistent with how we&#8217;ve always built the backup client: lightweight, unlimited, and focused on real user-generated files rather than duplicating data that already lives in the cloud.</p>



<h2 class="wp-block-heading">Where we&#8217;ve made it work, and where we&#8217;re still working</h2>



<p>We&#8217;ve successfully added support for iCloud Drive and Google Drive by working within those platforms&#8217; models. Extending the same support to every sync provider is more complex, but it&#8217;s something we&#8217;re actively exploring.</p>



<p>Files where third-party tools have not added reparse points or other placeholder indicators and are stored directly on a customer’s computer, outside of third-party sync folders, continue to be backed up as they always have been. We are actively evaluating how to better support data from synced sources in the future. If you have questions about your current backup coverage, you can read our Docs about <a href="https://www.backblaze.com/computer-backup/docs/back-up-third-party-application-data" rel="noreferrer noopener" target="_blank">backing up third-party application data,</a> or reach out to our Support team at <a href="mailto:helpme@backblaze.com" rel="noreferrer noopener" target="_blank">helpme@backblaze.com.</a></p>
<p>The post <a href="https://www.backblaze.com/blog/the-changing-landscape-of-cloud-sync-and-what-it-means-for-your-backup/">The Changing Landscape of Cloud Sync, and What It Means for Your Backup</a> appeared first on <a href="https://www.backblaze.com/blog">Backblaze Blog | Cloud Storage &amp; Cloud Backup</a></p>
