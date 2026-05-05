---
title: "Backblaze Performance Stats Q1 2026"
url: "https://www.backblaze.com/blog/backblaze-performance-stats-q1-2026/"
date: "Thu, 02 Apr 2026 13:00:00 +0000"
author: "Performance Stats Team"
feed_url: "https://www.backblaze.com/blog/feed/"
---
<figure class="wp-block-image size-full"><img alt="A decorative image with the title Q1 2026 Performance Stats. " class="wp-image-112862" height="820" src="https://backblaze.com/blog/wp-content/uploads/2026/04/Q1-2026-Performance-Stats-Blog-Header-1440x820-1.png" width="1440" /></figure>



<div class="wp-block-spacer" style="height: 15px;"></div>



<p>Cloud performance is easy to claim and hard to measure. As data volumes grow and workloads become more complex, the real question isn’t just how fast a provider is—it’s how that performance holds up in practice, and what you’re actually getting for what you pay.</p>



<p>Our answer to that challenge is Performance Stats, the most recent addition to our Stats franchises, Drive Stats and Network Stats. This ongoing, quarterly report will share performance testing results for both Backblaze and competitors, as well as the testing methodology so that anyone can recreate, compare results, and contribute to building better tests if necessary. (And, as always, we love the healthy debate in the comments section and beyond.)</p>



<p>By sharing the full results—strengths, limitations, anomalies, and more—we’re working to give developers and teams a more complete picture of how cloud storage providers perform in practice. We’re building a dataset over time, and we’re just at the beginning—let’s dive in.</p>



<div class="abstract" style="line-height: 1.8; margin: 24px 12px; padding: 24px 12px 10px 12px;">
<h4>And we can talk about it, too</h4>
Join the Performance Stats team on <a href="https://www.brighttalk.com/webcast/14807/665818" rel="">Thursday, April 9, 2026</a> to go over the stats, talk about testing methodology, and more. Have a question for us? Submit your question ahead of time <a href="https://docs.google.com/forms/d/e/1FAIpQLSdf42qZg-C7Px6msmtS4IHCWl59MO6_jj3-nakjA-ARZFowHg/viewform" rel="">here.</a>
<br />
<br />
<!--HubSpot Call-to-Action Code --><span class="hs-cta-wrapper" id="hs-cta-wrapper-b1b17bd8-7a8c-4430-8bbf-e82959b7c91f"><span class="hs-cta-node hs-cta-b1b17bd8-7a8c-4430-8bbf-e82959b7c91f" id="hs-cta-b1b17bd8-7a8c-4430-8bbf-e82959b7c91f"><!--[if lte IE 8]><div id="hs-cta-ie-element"></div><![endif]--><a href="https://cta-redirect.hubspot.com/cta/redirect/2832298/b1b17bd8-7a8c-4430-8bbf-e82959b7c91f" rel="noopener" target="_blank"><img alt="Register for the Webinar" class="hs-cta-img" id="hs-cta-img-b1b17bd8-7a8c-4430-8bbf-e82959b7c91f" src="https://no-cache.hubspot.com/cta/default/2832298/b1b17bd8-7a8c-4430-8bbf-e82959b7c91f.png" style="border-width: 0px;" /></a></span></span><!-- end HubSpot Call-to-Action Code --> 
</div>



<h2 class="wp-block-heading">Q1 2026: The results</h2>



<p>We ran performance testing for Backblaze B2, AWS S3, Cloudflare R2, and Wasabi Object Storage in two regions, US-East and the EU-Central. Our EU data center is in Amsterdam, and just like in our first round of testing, we matched the other cloud provider locations as closely as possible. You can jump to the testing methodology if you’d like more details.&nbsp;</p>



<p>Key findings:&nbsp;</p>



<ul class="wp-block-list">
<li><strong>Average upload and download times for US-East improved across nearly all providers and file sizes compared to Q4 2025.</strong> Backblaze led in upload averages for 256KiB and 5MiB files, with Wasabi taking the 2MiB category.</li>



<li><strong>Sustained throughput testing continues to tell a different story than averages alone.</strong> As with last quarter, the spread between highest and lowest values per file size remains wide—particularly in multi-threaded tests, where providers&#8217; architectural choices show up most clearly. </li>



<li><strong>EU-Central results show meaningful regional variation. </strong>Provider rankings shifted between US-East and EU-Central—for example, Cloudflare R2 performed notably well on EU upload and download averages, while Wasabi led in several EU upload throughput categories. The takeaway: geography matters, and no single provider&#8217;s US performance predicts their EU performance.</li>



<li><strong>Multi-threaded download tends to see a sharp rate of increase and then level out.</strong> In both US-East and the EU and for most of the tested providers, we see a sharp increase in mebibytes per second performance from the 256KiB to 5MiB file size, then a relatively flat trendline thereafter. This is an early trend that has existed quarter-on-quarter, and worth watching over time. </li>
</ul>



<p>And, here’s a roadmap if you want to quickly reach each test:&nbsp;</p>



<ul class="wp-block-list">
<li><a href="#US-East" id="#US-East" type="internal">US-East</a>
<ul class="wp-block-list">
<li><a href="#upload-comparison-US-east" id="#upload-comparison-US-east" type="internal">Upload averages (in milliseconds)</a></li>



<li><a href="#Five-minute-multi-threaded-upload-benchmark-US-east" id="#Five-minute-multi-threaded-upload-benchmark-US-east" type="internal">Five minute multi-threaded upload test</a></li>



<li><a href="#Five-minute-single-threaded-upload-test-US-east" id="#Five-minute-single-threaded-upload-test-US-east" type="internal">Five minute single-threaded upload test</a></li>



<li><a href="#Download-comparisons-US-east" id="#Download-comparisons-US-east" type="internal">Download averages and TTFB (in milliseconds)</a></li>



<li><a href="#Five-minute-multi-threaded-download-benchmark-US-East">Five minute multi-threaded download test</a></li>



<li><a href="#Five-minute-single-threaded-download-throughput-US-East" id="#Five-minute-single-threaded-download-throughput-US-East" type="internal">Five minute single-threaded download test</a></li>
</ul>
</li>



<li><a href="#EU-Central">EU-Central</a>
<ul class="wp-block-list">
<li><a href="#Upload-averages-EU-Central" id="#Upload-averages-EU-Central" type="internal">Upload averages (in milliseconds)</a></li>



<li><a href="#Five-minute-multi-threaded-upload-test-eu-central">Five minute multi-threaded upload test</a></li>



<li><a href="#Five-minute-single-threaded-upload-test-eu-central">Five minute single-threaded upload test</a></li>



<li><a href="#Download-averages-and-TTFB-eu-central">Download averages and TTFB (in milliseconds)</a></li>



<li><a href="#Five-minute-multi-threaded-download-test-eu-central">Five minute multi-threaded download test</a></li>



<li><a href="#Five-minute-single-threaded-download-test-eu-central">Five minute single-threaded download test</a></li>
</ul>
</li>
</ul>



<h2 class="wp-block-heading">A reminder of why we’re doing this</h2>



<p>We want to cut through the noise on cloud performance, and we’re working to build a transparent dataset to support that. This transparency is also why we’re publishing our testing methodology.&nbsp;</p>



<p>We want to take a hard look at performance on a level playing field for two reasons:&nbsp;</p>



<ol class="wp-block-list">
<li>Buyers should know what they&#8217;re getting and have the tools to sniff out the hype and misleading messaging many providers peddle about their performance. </li>



<li>If we don&#8217;t measure ourselves, we won&#8217;t get better. We want you to understand where we’re doing well today, and we want to take you along for the ride as we work to improve where we’re not. </li>
</ol>



<p>We’ve outlined the methodology at the end of this report. And, across the board, it’s important to note that this project is still young. Young datasets have lots of variability before they show true patterns: So, the best way to understand these results is to re-create them yourselves within your own tech stack.&nbsp;</p>



<h2 class="wp-block-heading">On the subject of transparency, let’s talk rate limits</h2>



<p>From the start, we expected the data to surface both strengths and weaknesses, which is why transparency has to include context—not just raw results. This time around, the thing that was revealed is <a href="https://www.backblaze.com/docs/en/cloud-storage-rate-limits" rel="noreferrer noopener" target="_blank">our rate limits</a>. </p>



<p>At a certain level of scale, cloud storage providers have to implement rate limits to ensure consistent performance and keep the platform secure from intentional or unintentional volumetric attacks. And, we even saw an example of that behavior <a href="https://www.backblaze.com/blog/backblaze-performance-stats-for-q3-2025/" rel="noreferrer noopener" target="_blank">last quarter</a> in the Wasabi data—in that case, the limit they have in place is that they don’t allow users to run HTTP requests for the first 30 days of a new account period. </p>



<p>Our rate limits work differently. I’m simplifying a bit, but there are three different ways you can trigger a rate limit: too much bandwidth being pushed, too many requests per second, or too many threads running concurrently. On the user’s side, you see either a 429 error (if you’re running our <a href="https://www.backblaze.com/docs/cloud-storage-native-api" rel="noreferrer noopener" target="_blank">B2 Native API</a>) or a 503 error (if you’re running the <a href="https://www.backblaze.com/docs/cloud-storage-s3-compatible-api" rel="noreferrer noopener" target="_blank">S3 compatible API</a>).</p>



<p>We didn’t hit rate limits in all tests. In fact, we only hit them in the multi-threaded throughput tests at the larger file sizes, which indicated to us that we were running into bandwidth caps. And, since throughput testing by nature <em>is </em>a stress test, this is relatively unsurprising. We’re trying to push as much data as possible in a five minute period—if the platform doesn’t know testing is happening, it can look like a volumetric attack.&nbsp;</p>



<p>Now to the sticky part from a reporting perspective: When we set out to write this report, the testing methodology includes the parameter that we’d test standard account tiers. In practice, we actually have no control over whether our testing accounts are being treated differently on the back-end with other providers, for better (preferential treatment) or worse (throttling). That’s also why we run testing from an independent Vultr server—it means we aren’t using a Backblaze-owned IP address, so the testing account isn’t identifiable by other providers. The accounts are being judged on their behavior.&nbsp;</p>



<p>So what do we do here? How do we balance testing against real world behavior? We decided to show you what it looks like when you hit rate limits and outline some potential steps for user-side mitigation.&nbsp;</p>



<p>On every cloud storage platform, we can expect that there are default rate limits applied. When we saw our own, we had the advantage of knowing that that’s what we were seeing—if we were in the real world, we’d do additional investigation to confirm. From a testing perspective, we went forward in a way that would be the most likely scenario in the real world: We incorporated an auto-retry script.&nbsp;</p>



<p>In all cases for this report, we were hitting bandwidth caps at the larger file sizes in the multi-threaded throughput tests. So, if the test tried and failed, we raised that limit and only that limit—all other account parameters stayed in line with the default standard account. In the real world, you would have completed your investigation, then reached out to <a href="https://www.backblaze.com/help">Support</a> to raise bandwidth caps, which would then apply to your account going forward.&nbsp;</p>



<p>There are actions you can take before requesting a change, especially because sometimes API calls are failing for other reasons. So it’s helpful to do things like retry with exponential backoff, double check your lifecycle rules and other automated processes (especially sequential operations), increase or decrease thread count, change file size, etc., and keep all the logs, too. Sometimes just those things will solve the issues you need to solve.&nbsp;</p>



<p>More importantly, all of those actions are things that will give you more information about what type of configuration issues you’re having, and, if you are running into a rate limit issue, (at least with us) you can request a specific configuration change. For example, in this case, we <em>only</em> raised the bandwidth cap, and kept all the other account configuration variables in line with our standard tier. Our concern was to keep the testing as fair and consistent as possible.&nbsp; But, in a real-world scenario, that may mean you’d avoid something like jumping into a different pricing tier. In all cases and with all providers, testing and communication are key at this stage. Data, as always, is king.&nbsp;</p>



<p>Back to this report: we have two important impacts. First, we can’t confidently make quarter over quarter comparisons this time around because we’ve changed the testing methodology (though we can do so in our upload and download averages, as they weren’t affected). We may point out observational patterns, but we can’t say they’re significant. And hey, the dataset is young—we shouldn’t be doing that yet anyway. Second, if we hit a rate limit, we went ahead and included that data as a separate line item in our tables—so I’ve updated our testing methodology accordingly.&nbsp;</p>



<p>With that out of the way, let’s get into the report.&nbsp;</p>



<h2 class="wp-block-heading" id="US-East">US-East</h2>



<p>This quarter, we’ve added a second region to our reporting. We’ll start with US-East, then move to EU-Central. </p>



<h3 class="wp-block-heading" id="upload-comparison-US-east">Upload comparisons</h3>



<p>This test shows the average time in milliseconds it takes to upload a file. Averages were taken across a month of data and for three different file sizes.</p>



<p>In these tests, a lower result is better, and as with the last report, we’ve highlighted the category winners in green for readability.</p>



<figure class="wp-block-image size-large wp-lightbox-container"><img alt="A chart showing average upload times for US-East. " class="wp-image-112863" height="717" src="https://backblaze.com/blog/wp-content/uploads/2026/04/1_US-EAST-Upload-Comparisons-1024x717.png" width="1024" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>



<p>We’ve got a young dataset here, so it’s hard to attribute significance this early, but let’s look at a quarter-over-quarter comparison. (Note: We did not have data from Wasabi last quarter.)</p>



<figure class="wp-block-image size-large wp-lightbox-container"><img alt="A chart showing a quarter on quarter comparison of average upload times for US-East." class="wp-image-112864" height="624" src="https://backblaze.com/blog/wp-content/uploads/2026/04/2_US-EAST-Upload-Comparisons-2-1024x624.png" width="1024" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>



<p>Interestingly, every provider had lower average upload times. Once again, Backblaze wins for 256KiB files. Last quarter, AWS led in the other two file sizes, but this quarter, Wasabi took over in the 2MiB category and Backblaze in the 5MiB.</p>



<h3 class="wp-block-heading" id="Five-minute-multi-threaded-upload-benchmark-US-east">Five minute multi-threaded upload benchmark</h3>



<p>In these tests, a higher result is better, as the result represents more average data being pushed in the five minute time period. This gives us quite a bit more information than just average upload time for a single file—it tells us the sustained amount of data you can push to a cloud storage provider in five minutes. This is also where we see our first rate limit in action.</p>



<figure class="wp-block-image size-large wp-lightbox-container"><img alt="A chart showing 5 minute multi-threaded upload benchmark times for US-East." class="wp-image-112865" height="752" src="https://backblaze.com/blog/wp-content/uploads/2026/04/3_US-EAST-5-Minute-Multi-Threaded-Upload-Benchmark-1-1024x752.png" width="1024" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>



<p>You’ll notice that the first two values for the rate limited and un-rate limited account are the same—which makes sense, because they hadn’t triggered the bandwidth cap. In the rate-limited version, the values in the higher file sizes are suspiciously similar. We had the benefit of knowing we were hitting our own rate limits, but if you were doing external testing, you’d go through the things we talked about above. Different providers have different policies on what they can and can’t allow, so check out each platform’s documentation for clarity.&nbsp;</p>



<p>As for the rest of the data: Wasabi sweeps this category. As our dataset grows over time, we’ll have more of an ability to say what’s “normal.” And, as always, your use case comes into play here—there’s a difference between baseline averages and what you can tolerate within your workflows, and when you’re making business decisions, the latter is where you find real value. <a href="https://www.backblaze.com/blog/escaping-egress-hidden-cloud-fees-every-cfo-should-know/" rel="noreferrer noopener" target="_blank">Trade-offs are strategy.</a> </p>



<p>While we can’t perfectly compare quarter-on-quarter because of the methodology change, it’s interesting to note that we still have a wide variance between our highest and our lowest values per file size category in this test type, which is in line with what we saw last quarter. If that pattern continues in future quarterly datasets, we should make sure we take it into account <a href="https://www.backblaze.com/blog/backblaze-drive-stats-for-q3-2025/" rel="noreferrer noopener" target="_blank">when interpreting outliers</a>. </p>



<p>Now let’s bring forward our alternative visualizations with the rate of increase:</p>



<figure class="wp-block-image size-large wp-lightbox-container"><img alt="A line graph showing 5 minute multi-threaded upload benchmark times for US-East." class="wp-image-112866" height="628" src="https://backblaze.com/blog/wp-content/uploads/2026/04/4_US-EAST-5-Minute-Multi-Threaded-Upload-Benchmark-2-1024x628.png" width="1024" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>



<p>And check in on clustering within the file sizes:</p>



<div class="wp-block-group is-content-justification-center is-nowrap is-layout-flex wp-container-core-group-is-layout-94bc23d7 wp-block-group-is-layout-flex">
<figure class="wp-block-image size-full is-resized wp-lightbox-container"><img alt="A chart showing 5 minute multi-threaded upload benchmark times for the 256KiB file size for US-East." class="wp-image-112867" height="728" src="https://backblaze.com/blog/wp-content/uploads/2026/04/5_US-EAST-5-Minute-Multi-Threaded-Upload-Benchmark-256KiB.png" style="width: 400px;" width="792" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>



<figure class="wp-block-image size-full is-resized wp-lightbox-container"><img alt="A chart showing 5 minute multi-threaded upload benchmark times for the 5MiB file size for US-East." class="wp-image-112868" height="742" src="https://backblaze.com/blog/wp-content/uploads/2026/04/6_US-EAST-5-Minute-Multi-Threaded-Upload-Benchmark-5MiB.png" style="width: 400px;" width="796" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>
</div>



<div class="wp-block-group is-content-justification-center is-nowrap is-layout-flex wp-container-core-group-is-layout-94bc23d7 wp-block-group-is-layout-flex">
<figure class="wp-block-image size-full is-resized wp-lightbox-container"><img alt="A chart showing 5 minute multi-threaded upload benchmark times for the 50MiB file size for US-East." class="wp-image-112869" height="742" src="https://backblaze.com/blog/wp-content/uploads/2026/04/7_US-EAST-5-Minute-Multi-Threaded-Upload-Benchmark-50MiB.png" style="width: 400px;" width="796" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>



<figure class="wp-block-image size-full is-resized wp-lightbox-container"><img alt="A chart showing 5 minute multi-threaded upload benchmark times for the 100MiB file size for US-East." class="wp-image-112870" height="742" src="https://backblaze.com/blog/wp-content/uploads/2026/04/8_US-EAST-5-Minute-Multi-Threaded-Upload-Benchmark-100MiB.png" style="width: 400px;" width="794" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>
</div>



<div class="wp-block-spacer" style="height: 15px;"></div>



<h3 class="wp-block-heading" id="Five-minute-single-threaded-upload-test-US-east">Five minute single threaded upload test</h3>



<p>Once again, higher is better in this result, and it measures the sustained amount of data you can push to a server in a single thread with different file sizes.</p>



<p>Multi-threaded tests reveal what happens when you parallelize workload or data transfer whereas a single-threaded test measures how efficiently a provider handles one request. So, from our perspective, single threaded operations show us how a provider handles overhead including connection setup (handshake), request routing, waiting for the first byte, and then actual data transfer. It matters when APIs are making sequential calls or you have latency-sensitive or small-object workloads.</p>



<figure class="wp-block-image size-large wp-lightbox-container"><img alt="A chart showing 5 minute single threaded upload benchmark times for US-East." class="wp-image-112871" height="719" src="https://backblaze.com/blog/wp-content/uploads/2026/04/9_US-EAST-5-Minute-Single-Threaded-Upload-Benchmark-1-1024x719.png" width="1024" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>



<p>In this test, Backblaze leads in the 256KiB, 50MiB, and 100MiB categories, and AWS leads in the 5MiB category. Here’s our line graph: </p>



<figure class="wp-block-image size-large wp-lightbox-container"><img alt="A line graph showing 5 minute single threaded upload benchmark times for US-East." class="wp-image-112872" height="552" src="https://backblaze.com/blog/wp-content/uploads/2026/04/10_US-EAST-Single-Threaded-Upload-Throughput-Test-1-1024x552.png" width="1024" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>



<p>And, like the multithreading results, we see a high degree of variance between our highest and lowest results, which becomes even more apparent in our clustered view:</p>



<div class="wp-block-group is-nowrap is-layout-flex wp-container-core-group-is-layout-ad2f72ca wp-block-group-is-layout-flex">
<figure class="wp-block-image size-full wp-lightbox-container"><img alt="A chart showing 5 minute single threaded upload benchmark times for the 256KiB file size for US-East." class="wp-image-112873" height="742" src="https://backblaze.com/blog/wp-content/uploads/2026/04/11_US-EAST-5-Minute-Single-Threaded-Upload-Benchmark-256KiB.png" width="792" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>



<figure class="wp-block-image size-full wp-lightbox-container"><img alt="A chart showing 5 minute single threaded upload benchmark times for the 5MiB file size for US-East." class="wp-image-112874" height="742" src="https://backblaze.com/blog/wp-content/uploads/2026/04/12_US-EAST-5-Minute-Single-Threaded-Upload-Benchmark-5MiB.png" width="792" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>
</div>



<div class="wp-block-group is-nowrap is-layout-flex wp-container-core-group-is-layout-ad2f72ca wp-block-group-is-layout-flex">
<figure class="wp-block-image size-full wp-lightbox-container"><img alt="A chart showing 5 minute single threaded upload benchmark times for the 50MiB file size for US-East." class="wp-image-112875" height="742" src="https://backblaze.com/blog/wp-content/uploads/2026/04/13_US-EAST-5-Minute-Single-Threaded-Upload-Benchmark-50MiB.png" width="788" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>



<figure class="wp-block-image size-full wp-lightbox-container"><img alt="A chart showing 5 minute single threaded upload benchmark times for the 100MiB file size for US-East." class="wp-image-112876" height="742" src="https://backblaze.com/blog/wp-content/uploads/2026/04/14_US-EAST-5-Minute-Single-Threaded-Upload-Benchmark-100MiB.png" width="794" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>
</div>



<div class="wp-block-spacer" style="height: 15px;"></div>



<h3 class="wp-block-heading" id="Download-comparisons-US-east">Download comparisons and TTFB</h3>



<p>As with our upload average data, lower is better. This test measures how long it takes a single file to download, on average.</p>



<figure class="wp-block-image size-large wp-lightbox-container"><img alt="A chart showing average download times for US-East." class="wp-image-112877" height="754" src="https://backblaze.com/blog/wp-content/uploads/2026/04/15_US-EAST-Download-comparison-1-1024x754.png" width="1024" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>



<p>Last quarter, AWS led in all file sizes. This quarter, Backblaze overtakes in the 2MiB category, while Amazon S3 still leads in time to first byte (TTFB) as well as the 256KiB and 5MiB file sizes. Let’s zoom in on time to first byte (TTFB). </p>



<figure class="wp-block-image size-large wp-lightbox-container"><img alt="A chart showing time to first byte for US-East." class="wp-image-112878" height="715" src="https://backblaze.com/blog/wp-content/uploads/2026/04/16_US-EAST-Time-to-first-byte-1024x715.png" width="1024" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>



<p>And take a look at our QoQ comparison:</p>



<figure class="wp-block-image size-large wp-lightbox-container"><img alt="A chart showing a quarter on quarter comparison of average download times for US-East." class="wp-image-112879" height="643" src="https://backblaze.com/blog/wp-content/uploads/2026/04/17_US-EAST-Download-comparison-2-1024x643.png" width="1024" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>



<p>Again, our dataset is too young to determine the significance of changes within each category. Observationally, it’s interesting to note that most of these numbers improved.</p>



<h3 class="wp-block-heading" id="Five-minute-multi-threaded-download-benchmark-US-East">Five minute multi-threaded download benchmark</h3>



<p>In these tests, a higher result is better, as the result represents more average data being downloaded in the five minute time period. And, as above, we can see Backblaze rate limits in the data. </p>



<figure class="wp-block-image size-large wp-lightbox-container"><img alt="A chart showing 5 minute multi-threaded download benchmark times for US-East." class="wp-image-112880" height="791" src="https://backblaze.com/blog/wp-content/uploads/2026/04/18_US-EAST-5-Minute-Multi-Threaded-Download-Benchmark-1-1024x791.png" width="1024" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>



<p>Backblaze leads for 256KiB files, AWS for 5MiB and 50MiB files, and Cloudflare for 100MiB files.</p>



<p>Let’s give ourselves the same charts as our upload tests. Here’s the trendline:&nbsp;</p>



<figure class="wp-block-image size-large wp-lightbox-container"><img alt="A line graph showing 5 minute multi-threaded download benchmark times for US-East." class="wp-image-112881" height="527" src="https://backblaze.com/blog/wp-content/uploads/2026/04/19_US-EAST-5-Minute-Multi-Threaded-Download-Benchmark-2-1024x527.png" width="1024" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>



<p>This chart makes clear how comparatively well Cloudflare R2 does at the larger file sizes—and as their core business is CDN, that makes a lot of strategic sense.&nbsp;</p>



<p>Here’s the per-file size clustering:&nbsp;</p>



<div class="wp-block-group is-nowrap is-layout-flex wp-container-core-group-is-layout-ad2f72ca wp-block-group-is-layout-flex">
<figure class="wp-block-image size-full wp-lightbox-container"><img alt="A chart showing 5 minute multi-threaded download benchmark times for the 256KiB file size for US-East." class="wp-image-112882" height="736" src="https://backblaze.com/blog/wp-content/uploads/2026/04/20_US-EAST-5-Minute-Multi-Threaded-Download-Benchmark-256KiB.png" width="792" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>



<figure class="wp-block-image size-full wp-lightbox-container"><img alt="A chart showing 5 minute multi-threaded download benchmark times for the 5MiB file size for US-East." class="wp-image-112883" height="742" src="https://backblaze.com/blog/wp-content/uploads/2026/04/21_US-EAST-5-Minute-Multi-Threaded-Download-Benchmark-5MiB.png" width="790" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>
</div>



<div class="wp-block-group is-nowrap is-layout-flex wp-container-core-group-is-layout-ad2f72ca wp-block-group-is-layout-flex">
<figure class="wp-block-image size-full wp-lightbox-container"><img alt="A chart showing 5 minute multi-threaded download benchmark times for the 50MiB file size for US-East." class="wp-image-112884" height="742" src="https://backblaze.com/blog/wp-content/uploads/2026/04/22_US-EAST-5-Minute-Multi-Threaded-Download-Benchmark-50MiB.png" width="788" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>



<figure class="wp-block-image size-full wp-lightbox-container"><img alt="A chart showing 5 minute multi-threaded download benchmark times for the 100MiB file size for US-East." class="wp-image-112885" height="728" src="https://backblaze.com/blog/wp-content/uploads/2026/04/23_US-EAST-5-Minute-Multi-Threaded-Download-Benchmark-100MiB.png" width="786" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>
</div>



<div class="wp-block-spacer" style="height: 15px;"></div>



<h3 class="wp-block-heading" id="Five-minute-single-threaded-download-throughput-US-East">Five minute single-threaded download throughput</h3>



<figure class="wp-block-image size-large wp-lightbox-container"><img alt="A chart showing 5 minute single threaded download benchmark times for US-East." class="wp-image-112886" height="723" src="https://backblaze.com/blog/wp-content/uploads/2026/04/24_US-EAST-5-Minute-Single-Threaded-Download-Benchmark-1-1024x723.png" width="1024" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>



<p>Wasabi comes in first for 256KiB and 5MiB files, and Backblaze for 50MiB and 100MiB files.</p>



<figure class="wp-block-image size-large"><a href="https://backblaze.com/blog/wp-content/uploads/2026/04/25_US-EAST-5-Minute-Single-Threaded-Download-Benchmark-2.png" title="25_[US EAST] 5 Minute Single Threaded Download Benchmark 2"><img alt="A line graph showing 5 minute single threaded download benchmark times for US-East." class="wp-image-112887" height="519" src="https://backblaze.com/blog/wp-content/uploads/2026/04/25_US-EAST-5-Minute-Single-Threaded-Download-Benchmark-2-1024x519.png" width="1024" /></a></figure>



<p>And here’s our clustering:</p>



<div class="wp-block-group is-nowrap is-layout-flex wp-container-core-group-is-layout-ad2f72ca wp-block-group-is-layout-flex">
<figure class="wp-block-image size-full wp-lightbox-container"><img alt="A chart showing 5 minute single threaded download benchmark times for the 256KiB file size for US-East." class="wp-image-112888" height="742" src="https://backblaze.com/blog/wp-content/uploads/2026/04/26_US-EAST-5-Minute-Single-Threaded-Download-Benchmark-256KiB.png" width="796" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>



<figure class="wp-block-image size-full wp-lightbox-container"><img alt="A chart showing 5 minute single threaded download benchmark times for the 5MiB file size for US-East." class="wp-image-112889" height="742" src="https://backblaze.com/blog/wp-content/uploads/2026/04/27_US-EAST-5-Minute-Single-Threaded-Download-Benchmark-5MiB.png" width="786" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>
</div>



<div class="wp-block-group is-nowrap is-layout-flex wp-container-core-group-is-layout-ad2f72ca wp-block-group-is-layout-flex">
<figure class="wp-block-image size-full wp-lightbox-container"><img alt="A chart showing 5 minute single threaded download benchmark times for the 50MiB file size for US-East." class="wp-image-112890" height="742" src="https://backblaze.com/blog/wp-content/uploads/2026/04/28_US-EAST-5-Minute-Single-Threaded-Download-Benchmark-50MiB.png" width="792" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>



<figure class="wp-block-image size-full wp-lightbox-container"><img alt="A chart showing 5 minute single threaded download benchmark times for the 100MiB file size for US-East." class="wp-image-112891" height="742" src="https://backblaze.com/blog/wp-content/uploads/2026/04/29_US-EAST-5-Minute-Single-Threaded-Download-Benchmark-100MiB.png" width="786" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>
</div>



<div class="wp-block-spacer" style="height: 15px;"></div>



<h2 class="wp-block-heading" id="EU-Central">EU-Central</h2>



<p>Welcome to the new region! We’ll keep editorializing to a minimum—here’s the EU data.</p>



<h3 class="wp-block-heading" id="Upload-averages-EU-Central">Upload averages </h3>



<figure class="wp-block-image size-large wp-lightbox-container"><img alt="A chart showing average upload times for EU-Central." class="wp-image-112893" height="712" src="https://backblaze.com/blog/wp-content/uploads/2026/04/30_-EU-CENTRAL-Upload-Averages-1024x712.png" width="1024" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>



<p>In this test, Cloudflare R2 takes the 256KiB category, while Backblaze is the fastest for both 2MiB and 5MiB file sizes. It’s tempting to compare these numbers to the US-East performance, but certainly premature. </p>



<p>At the very least, it’s a good reminder of the strength of a multi-cloud approach—there’s always a balance between <a href="https://www.backblaze.com/blog/how-neocloud-alliances-reduce-the-internets-largest-single-point-of-failure/" rel="noreferrer noopener" target="_blank">relying on a single provider</a> regardless of their geographic presence or their strength in your particular use case needs.  Specialists bring value to the table if and when their addition doesn’t <a href="https://www.backblaze.com/blog/why-build-is-a-bigger-distraction-than-you-think-for-neoclouds/" rel="noreferrer noopener" target="_blank">outweigh the operational costs of complexity</a>.</p>



<h3 class="wp-block-heading" id="Five-minute-multi-threaded-upload-test-eu-central">Five minute multi-threaded upload test</h3>



<p>Top of section reminder: Higher is better in this test.</p>



<figure class="wp-block-image size-large wp-lightbox-container"><img alt="A chart showing 5 minute multi-threaded upload benchmark times for EU-Central." class="wp-image-112895" height="706" src="https://backblaze.com/blog/wp-content/uploads/2026/04/31_EU-CENTRAL-Multi-threaded-005-upload-throughput-1024x706.png" width="1024" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>



<p>In these results, Wasabi leads in the 256KiB and 100MiB categories, while AWS wins out for the 5MiB and 50MiB file sizes.&nbsp;</p>



<p>Here’s the trendline:</p>



<figure class="wp-block-image size-large wp-lightbox-container"><img alt="A line graph showing 5 minute multi-threaded upload benchmark times for EU-Central." class="wp-image-112896" height="475" src="https://backblaze.com/blog/wp-content/uploads/2026/04/32_EU-CENTRAL-Multi-threaded-005-upload-throughput-2-1024x475.png" width="1024" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>



<p>And here’s the by-file-size clustering:</p>



<div class="wp-block-group is-nowrap is-layout-flex wp-container-core-group-is-layout-ad2f72ca wp-block-group-is-layout-flex">
<figure class="wp-block-image size-full wp-lightbox-container"><img alt="A chart showing 5 minute multi-threaded upload benchmark times for the 256KiB file size for EU-Central." class="wp-image-112897" height="730" src="https://backblaze.com/blog/wp-content/uploads/2026/04/33_EU-CENTRAL-Multi-threaded-005-upload-throughput-256KiB.png" width="790" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>



<figure class="wp-block-image size-full wp-lightbox-container"><img alt="A chart showing 5 minute multi-threaded upload benchmark times for the 5MiB file size for EU-Central." class="wp-image-112898" height="730" src="https://backblaze.com/blog/wp-content/uploads/2026/04/34_EU-CENTRAL-Multi-threaded-005-upload-throughput-5MiB.png" width="790" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>
</div>



<div class="wp-block-group is-nowrap is-layout-flex wp-container-core-group-is-layout-ad2f72ca wp-block-group-is-layout-flex">
<figure class="wp-block-image size-full wp-lightbox-container"><img alt="A chart showing 5 minute multi-threaded upload benchmark times for the 50MiB file size for EU-Central." class="wp-image-112899" height="730" src="https://backblaze.com/blog/wp-content/uploads/2026/04/35_EU-CENTRAL-Multi-threaded-005-upload-throughput-50MiB.png" width="798" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>



<figure class="wp-block-image size-full wp-lightbox-container"><img alt="A chart showing 5 minute multi-threaded upload benchmark times for the 100MiB file size for EU-Central." class="wp-image-112900" height="742" src="https://backblaze.com/blog/wp-content/uploads/2026/04/36_EU-CENTRAL-Multi-threaded-005-upload-throughput-100MiB.png" width="794" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>
</div>



<div class="wp-block-spacer" style="height: 15px;"></div>



<h3 class="wp-block-heading" id="Five-minute-single-threaded-upload-test-eu-central">Five minute single-threaded upload test</h3>



<figure class="wp-block-image size-large wp-lightbox-container"><img alt="A chart showing 5 minute single threaded upload benchmark times for EU-Central." class="wp-image-112901" height="772" src="https://backblaze.com/blog/wp-content/uploads/2026/04/37_EU-CENTRAL-5-Minute-Single-Threaded-Upload-Benchmark-1-1024x772.png" width="1024" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>



<p>Wasabi dominates this category. Backblaze is a close second for the smallest file size, and S3 takes second for both the 50MiB and 100MiB categories.</p>



<figure class="wp-block-image size-large wp-lightbox-container"><img alt="A line graph showing 5 minute single threaded upload benchmark times for EU-Central." class="wp-image-112902" height="562" src="https://backblaze.com/blog/wp-content/uploads/2026/04/38_EU-CENTRAL-5-Minute-Single-Threaded-Upload-Benchmark-2-1024x562.png" width="1024" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>



<div class="wp-block-group is-nowrap is-layout-flex wp-container-core-group-is-layout-ad2f72ca wp-block-group-is-layout-flex">
<figure class="wp-block-image size-full wp-lightbox-container"><img alt="A chart showing 5 minute single threaded upload benchmark times for the 256KiB file size for EU-Central." class="wp-image-112903" height="742" src="https://backblaze.com/blog/wp-content/uploads/2026/04/39_EU-CENTRAL-5-Minute-Single-Threaded-Upload-Benchmark-256KiB.png" width="796" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>



<figure class="wp-block-image size-full wp-lightbox-container"><img alt="A chart showing 5 minute single threaded upload benchmark times for the 5MiB file size for EU-Central." class="wp-image-112904" height="742" src="https://backblaze.com/blog/wp-content/uploads/2026/04/40_EU-CENTRAL-5-Minute-Single-Threaded-Upload-Benchmark-5MiB.png" width="794" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>
</div>



<div class="wp-block-group is-nowrap is-layout-flex wp-container-core-group-is-layout-ad2f72ca wp-block-group-is-layout-flex">
<figure class="wp-block-image size-full wp-lightbox-container"><img alt="A chart showing 5 minute single threaded upload benchmark times for the 50MiB file size for EU-Central." class="wp-image-112905" height="742" src="https://backblaze.com/blog/wp-content/uploads/2026/04/41_EU-CENTRAL-5-Minute-Single-Threaded-Upload-Benchmark-50MiB.png" width="796" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>



<figure class="wp-block-image size-full wp-lightbox-container"><img alt="A chart showing 5 minute single threaded upload benchmark times for the 100MiB file size for EU-Central." class="wp-image-112906" height="742" src="https://backblaze.com/blog/wp-content/uploads/2026/04/42_EU-CENTRAL-5-Minute-Single-Threaded-Upload-Benchmark-100MiB.png" width="794" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>
</div>



<h3 class="wp-block-heading" id="Download-averages-and-TTFB-eu-central">Download averages and TTFB </h3>



<figure class="wp-block-image size-large wp-lightbox-container"><img alt="A chart showing average download times for EU-Central." class="wp-image-112907" height="747" src="https://backblaze.com/blog/wp-content/uploads/2026/04/43_EU-CENTRAL-Download-Averages-1024x747.png" width="1024" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>



<p>Cloudflare performs well in this region, with the fastest average times in TTFB, 256KiB, and 2MiB categories. AWS wins on the remaining 5MiB file size. Here again we see a huge delta between the highest and lowest average times.&nbsp;</p>



<p>And, here’s our TTFB chart:</p>



<figure class="wp-block-image size-large wp-lightbox-container"><img alt="A chart showing time to first byte for EU-Central." class="wp-image-112908" height="665" src="https://backblaze.com/blog/wp-content/uploads/2026/04/44_EU-CENTRAL-ttfb-EU-Download-Averages-1024x665.png" width="1024" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>



<p>Just like in the <a href="https://www.backblaze.com/cloud-storage/resources/hard-drive-test-data" rel="noreferrer noopener" target="_blank">Drive Stats series</a>, when we see numbers like this, we do some internal investigation—comparative numbers show us where we can improve, which is why this testing is so critical. We&#8217;ve identified an issue we believe was contributing; we&#8217;ll report on the impact of our fixes in a future report.</p>



<h3 class="wp-block-heading" id="Five-minute-multi-threaded-download-test-eu-central">Five minute multi-threaded download test</h3>



<figure class="wp-block-image size-large wp-lightbox-container"><img alt="A chart showing 5 minute multi-threaded download benchmark times for EU-Central." class="wp-image-112909" height="901" src="https://backblaze.com/blog/wp-content/uploads/2026/04/45_EU-CENTRAL-5-Minute-Multi-Threaded-Download-Benchmark-1-1024x901.png" width="1024" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>



<p>Backblaze leads in the 256KiB file size, while AWS leads in the other three categories. Let’s look at our alternate views. </p>



<figure class="wp-block-image size-large wp-lightbox-container"><img alt="A line graph showing 5 minute multi-threaded download benchmark times for EU-Central." class="wp-image-112910" height="830" src="https://backblaze.com/blog/wp-content/uploads/2026/04/46_EU-CENTRAL-5-Minute-Multi-Threaded-Download-Throughput-Test-2-1024x830.png" width="1024" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>



<div class="wp-block-group is-nowrap is-layout-flex wp-container-core-group-is-layout-ad2f72ca wp-block-group-is-layout-flex">
<figure class="wp-block-image size-full wp-lightbox-container"><img alt="A chart showing 5 minute multi-threaded download benchmark times for the 256KiB file size for EU-Central." class="wp-image-112911" height="742" src="https://backblaze.com/blog/wp-content/uploads/2026/04/47_EU-CENTRAL-5-Minute-Multi-Threaded-Download-Benchmark-256KiB.png" width="794" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>



<figure class="wp-block-image size-full wp-lightbox-container"><img alt="A chart showing 5 minute multi-threaded download benchmark times for the 5MiB file size for EU-Central." class="wp-image-112912" height="742" src="https://backblaze.com/blog/wp-content/uploads/2026/04/48_EU-CENTRAL-5-Minute-Multi-Threaded-Download-Benchmark-5MiB.png" width="794" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>
</div>



<div class="wp-block-group is-nowrap is-layout-flex wp-container-core-group-is-layout-ad2f72ca wp-block-group-is-layout-flex">
<figure class="wp-block-image size-full wp-lightbox-container"><img alt="A chart showing 5 minute multi-threaded download benchmark times for the 50MiB file size for EU-Central." class="wp-image-112913" height="742" src="https://backblaze.com/blog/wp-content/uploads/2026/04/49_EU-CENTRAL-5-Minute-Multi-Threaded-Download-Benchmark-50MiB.png" width="798" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>



<figure class="wp-block-image size-full wp-lightbox-container"><img alt="A chart showing 5 minute multi-threaded download benchmark times for the 100MiB file size for EU-Central." class="wp-image-112914" height="742" src="https://backblaze.com/blog/wp-content/uploads/2026/04/50_EU-CENTRAL-5-Minute-Multi-Threaded-Download-Benchmark-100MiB.png" width="794" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>
</div>



<div class="wp-block-spacer" style="height: 15px;"></div>



<h3 class="wp-block-heading" id="Five-minute-single-threaded-download-test-eu-central">Five minute single-threaded download test</h3>



<figure class="wp-block-image size-large wp-lightbox-container"><img alt="A chart showing 5 minute single threaded download benchmark times for US-East." class="wp-image-112915" height="749" src="https://backblaze.com/blog/wp-content/uploads/2026/04/51_EU-CENTRAL-5-Minute-Single-Threaded-Download-Benchmark-1024x749.png" width="1024" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>



<p>Wasabi comes first in the 256KiB file size, while AWS leads in all other categories. Here’s the trendline:</p>



<figure class="wp-block-image size-large wp-lightbox-container"><img alt="A line graph showing 5 minute single threaded download benchmark times for US-East." class="wp-image-112916" height="571" src="https://backblaze.com/blog/wp-content/uploads/2026/04/52_EU-CENTRAL-5-MinuteSingle-Threaded-Download-Throughput-Test-1024x571.png" width="1024" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>



<p>And our clustering:</p>



<div class="wp-block-group is-nowrap is-layout-flex wp-container-core-group-is-layout-ad2f72ca wp-block-group-is-layout-flex">
<figure class="wp-block-image size-full wp-lightbox-container"><img alt="A chart showing 5 minute single threaded download benchmark times for the 256KiB file size for US-East." class="wp-image-112917" height="742" src="https://backblaze.com/blog/wp-content/uploads/2026/04/53_EU-CENTRAL-5-Minute-Single-Threaded-Download-Benchmark-256KiB.png" width="794" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>



<figure class="wp-block-image size-full wp-lightbox-container"><img alt="A chart showing 5 minute single threaded download benchmark times for the 5MiB file size for US-East." class="wp-image-112918" height="742" src="https://backblaze.com/blog/wp-content/uploads/2026/04/54_EU-CENTRAL-5-Minute-Single-Threaded-Download-Benchmark-5MiB.png" width="792" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>
</div>



<div class="wp-block-group is-nowrap is-layout-flex wp-container-core-group-is-layout-ad2f72ca wp-block-group-is-layout-flex">
<figure class="wp-block-image size-full wp-lightbox-container"><img alt="A chart showing 5 minute single threaded download benchmark times for the 50MiB file size for US-East." class="wp-image-112919" height="742" src="https://backblaze.com/blog/wp-content/uploads/2026/04/55_EU-CENTRAL-5-Minute-Single-Threaded-Download-Benchmark-50MiB.png" width="792" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>



<figure class="wp-block-image size-full wp-lightbox-container"><img alt="" class="wp-image-112920" height="742" src="https://backblaze.com/blog/wp-content/uploads/2026/04/56_EU-CENTRAL-5-Minute-Single-Threaded-Download-Benchmark-100MiB.png" width="796" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>
</div>



<h2 class="wp-block-heading">Test methodology</h2>



<p>Our goal with these benchmarks is simple: to understand how our cloud performs under real-world conditions and to share that information as clearly as possible. To do that, our Cloud Operations team runs repeatable, synthetic tests that measure upload (PUT) and download (GET) performance.&nbsp;</p>



<p>We ran both upload and download tests across all six vendors. Upload tests measured average total time to download a single file of the following file sizes:</p>



<ul class="wp-block-list">
<li>256KiB</li>



<li>2MiB</li>



<li>5MiB</li>
</ul>



<p>Download tests measured:</p>



<ul class="wp-block-list">
<li>Time-to-first-byte (TTFB)</li>



<li>Average total time to download the following file sizes:
<ul class="wp-block-list">
<li>256KiB</li>



<li>2MiB</li>



<li>5MiB</li>
</ul>
</li>
</ul>



<p>Throughput tests run in five-minute profiles to observe consistency over time, and we ran both single and multi-threaded upload and download tests. From a practical perspective, what’s happening in this test is that we’re pushing repeated requests to a cloud storage provider as many times as we can for five minutes. In multi-threaded tests, we run 20 concurrent threads. Throughput tests use the following file sizes:&nbsp;</p>



<ul class="wp-block-list">
<li>256KiB</li>



<li>5MiB</li>



<li>50MiB </li>



<li>100MiB</li>
</ul>



<p>All tests originate from a Vultr-hosted Ubuntu virtual machine (VM) located in the respective test regions (US-East and EU-Central), routing through Catchpoint’s network into the object storage regions. By keeping the source environment stable and the test target consistent, we isolate performance variables within each provider’s infrastructure rather than the test environment itself.</p>



<h3 class="wp-block-heading">Consistency measures</h3>



<p>To ensure each test result represents genuine performance rather than environmental noise, we built repeatability into the process:</p>



<ul class="wp-block-list">
<li><strong>Identical test instances:</strong> All runs used the same VM type, operating system (OS) image, and configuration.</li>



<li><strong>Fixed regions:</strong> Tests originated from the same location (NY/NJ) targeting the same US-East or EU-Central region across providers.</li>



<li><strong>Controlled routing:</strong> Network paths were held constant through Catchpoint’s monitoring network to minimize geographic or peering variation.</li>



<li><strong>Repeated runs: </strong>Each test profile (5 min) was executed multiple times, and averages were used to reduce the impact of transient spikes.</li>



<li><strong>Standardized payloads: </strong>All uploads and downloads used identical objects to ensure a consistent file-size baseline.</li>



<li><strong>Unchanged test intervals: </strong>Tests were scheduled at regular intervals over multiple days to capture both typical and outlier performance.</li>
</ul>



<h3 class="wp-block-heading">About synthetic testing</h3>



<p>Synthetic monitoring provides a controlled, apples-to-apples comparison, but it doesn’t replicate every production workload. These tests are run outside our own infrastructure—from neutral vantage points—to simulate a customer’s experience at the “last mile.” This distinguishes our approach from competitors who benchmark internally under optimized conditions.</p>



<p>It’s important to note that synthetic results won’t mirror every customer’s experience. Different architectures, connection paths, and file patterns will produce different performance profiles. Our intent is to offer transparency into the methodology and relative behaviors, not to suggest that all workloads will perform identically.</p>



<h2 class="wp-block-heading">Limitations and future work</h2>



<p>Every benchmark is an approximation. These results provide a controlled look at how cloud storage performs under repeatable conditions, but they don’t capture every variable in production environments. Below, we outline what our current tests don’t measure and where we’re headed next to deepen the picture.</p>



<ul class="wp-block-list">
<li><strong>Synthetic, not real-world workloads: </strong>These benchmarks simulate real activity but don’t reproduce the full variability of customer workloads, concurrency levels, or data locality patterns. They are best understood as directional insights rather than absolute truths.</li>



<li><strong>The internet is the internet:</strong> Once traffic leaves the test node, we can’t control the routing, peering, or transient network conditions between endpoints. Each provider’s own network policies and routing optimizations—for example, Wasabi’s inbound connection rules—can influence the results.</li>



<li><strong>File size constraints:</strong> Our testing environment currently limits file sizes to 10MiB or smaller due to timeout thresholds. That means we can’t yet model the large-object transfers typical of certain workloads.</li>



<li><strong>Static test conditions:</strong> All tests were conducted from a single region (NY/NJ to US-East cloud providers). Real-world customers operate globally, where peering arrangements, congestion, and latency differ widely.</li>



<li><strong>Potential caching effects: </strong>Although we designed the tests to avoid cached reads, Catchpoint does not allow full data randomization. It’s possible some repeated reads benefited from intermediate caching at any network layer. </li>



<li><strong>Traffic shaping and rate limiting:</strong> Providers may apply rate limits or throttling when detecting high-frequency test traffic. For example, Wasabi temporarily blacklisted our IPs due to testing volume—a reminder that these results represent observed behavior, not formal service guarantees.</li>
</ul>



<h2 class="wp-block-heading">Your mileage may vary, or what this means in the real world</h2>



<p>One of the reasons it&#8217;s so hard to get directly comparable performance benchmarks is because there are so many configurable elements on the user&#8217;s side that can affect the results. For example, if you know that your provider is faster on smaller files, you might choose to store your unstructured data in smaller parts so that you achieve faster performance.&nbsp;</p>



<p>We did some comparison between existing use cases that Backblaze succeeds based on the data above including AI/ML inference, feature stores and embedding lookups, LLM-based RAG systems, log and event analytics, interactive data lake querying, and CDN origin. The biggest takeaway is something that we noted when talking about the EU metrics—specialists bring flexibility to the table, which is where you truly start to unlock value. </p>



<p>For a cloud storage provider, tracking these metrics over time and comparing to other aspects of our internal architecture enables us to support ongoing and <a href="https://www.backblaze.com/blog/analyzing-performance-at-exabyte-scale/" rel="noreferrer noopener" target="_blank">continual performance improvement,</a> and to understand how much of an impact single changes might make. This means that what seems like a simple project to <a href="https://www.backblaze.com/blog/one-simple-change-that-made-our-exabyte-scale-storage-faster/" rel="noreferrer noopener" target="_blank">change the way we read header requests</a> can produce asymmetrically favorable results.</p>



<h2 class="wp-block-heading">What’s next?</h2>



<p>Performance is an evolving target, and this dataset is still early. What we can say today is directional: different providers behave differently under different conditions, and those differences become more pronounced as workloads scale.</p>



<p>We’ll keep expanding this work in future reports—across regions, workloads, and test conditions—with the expectation that clearer patterns will emerge. In the meantime, the most valuable use of this data is to map it against your own systems, your own constraints, and your own definition of performance.</p>



<p>If you’re doing that, we’d like to hear what you’re seeing. Sound off in the comments below, on <a href="https://www.linkedin.com/company/backblaze/" rel="noreferrer noopener" target="_blank">socials</a>, drop us a line <a href="mailto:drivestats@backblaze.com" rel="noreferrer noopener" target="_blank">by email</a>, or <a href="https://docs.google.com/forms/d/e/1FAIpQLSdf42qZg-C7Px6msmtS4IHCWl59MO6_jj3-nakjA-ARZFowHg/viewform?usp=publish-editor" rel="noreferrer noopener" target="_blank">send us some questions</a> you want answered in the <a href="https://www.brighttalk.com/webcast/14807/665818" rel="noreferrer noopener" target="_blank">upcoming webinar</a>. </p>
<p>The post <a href="https://www.backblaze.com/blog/backblaze-performance-stats-q1-2026/">Backblaze Performance Stats Q1 2026</a> appeared first on <a href="https://www.backblaze.com/blog">Backblaze Blog | Cloud Storage &amp; Cloud Backup</a></p>
