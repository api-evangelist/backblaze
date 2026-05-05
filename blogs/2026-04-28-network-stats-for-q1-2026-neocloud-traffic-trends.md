---
title: "Network Stats for Q1 2026: Neocloud Traffic Trends"
url: "https://www.backblaze.com/blog/network-stats-for-q1-2026-neocloud-traffic-trends/"
date: "Tue, 28 Apr 2026 13:00:00 +0000"
author: "Brent Nowak"
feed_url: "https://www.backblaze.com/blog/feed/"
---
<figure class="wp-block-image size-full"><img alt="A decorative image with the words Q1 2026 Network Stats. " class="wp-image-112947" height="820" src="https://backblaze.com/blog/wp-content/uploads/2026/04/Q1-2026-Network-Stats-Blog-Header-1440x820-1.png" width="1440" /></figure>



<div class="wp-block-spacer" style="height: 15px;"></div>



<p>Welcome to our second quarterly Network Stats report covering Q1 of 2026. Along with <a href="https://www.backblaze.com/blog/backblaze-drive-stats-for-q3-2025/" rel="noreferrer noopener" target="_blank">Drive Stats</a> and <a href="https://www.backblaze.com/blog/backblaze-performance-stats-for-q3-2025/" rel="noreferrer noopener" target="_blank">Performance Stats</a>, Network Stats pulls back the curtain on real-world infrastructure data, particularly how network-level analytics reflect emerging AI industry trends and usage patterns. </p>



<div class="wp-block-group has-background" style="background-color: #f5f4ff;"><div class="wp-block-group__inner-container is-layout-constrained wp-block-group-is-layout-constrained">
<h4 class="wp-block-heading">Get more Network Stats (and the details of the dataset)</h4>



<p>If you are curious about what metrics we’re recording and how we classify data in <a href="https://www.backblaze.com/blog/networkstats">this series</a>, check out the details outlined in our <a href="https://www.backblaze.com/blog/network-stats-for-q3-2025-the-magnitude-of-ai-workflows/">Q3 2025 Network Stats </a> and Q4 2025 Network Stats report.</p>
</div></div>



<div class="wp-block-spacer" style="height: 10px;"></div>



<p>One of the roles of the Network Engineering (NetEng) team at Backblaze is to monitor how traffic moves into, out of, and across our platform—not just day-to-day, but over time as customer behavior and industry dynamics evolve. Right now, few forces are reshaping networks faster than AI.&nbsp;</p>



<p>With the launch of <a href="https://www.backblaze.com/cloud-storage/b2-overdrive" rel="noreferrer noopener" target="_blank">B2 Overdrive</a> in April 2025, we built a direct, high-performance path between our storage layers and neoclouds where processing, inference, and modeling take place. It has given us a front-row seat to the impact of AI and how network behavior is changing with it. This quarter, in addition to our regular data analysis, we’ve added some geographic heatmaps to understand where and how data is moving. </p>



<div class="abstract" style="line-height: 1.8; margin: 24px 12px; padding: 24px 12px 10px 12px;">
<h4>Join us live for the webinar</h4>

<p>Join us live for the <a href="https://www.brighttalk.com/webcast/14807/667297?utm_source=Backblaze&#038;utm_medium=brighttalk&#038;utm_campaign=667297" rel="">Q1 2026 Network Stats webinar</a>Monday, May 4, 2026 at 11:30 a.m. PT / 2:30 p.m. PT. We’ll explore where AI traffic concentrates, how high-magnitude data flows behave, and what early indicators suggest about the future of AI-native infrastructure design.</p>

<p>Can’t make it live, or reading this article after-the-fact? <a href="https://www.brighttalk.com/webcast/14807/667297?utm_source=Backblaze&#038;utm_medium=brighttalk&#038;utm_campaign=667297" rel="">Sign up anyway</a> and catch the recording on demand.</p> 

<!--HubSpot Call-to-Action Code --><span class="hs-cta-wrapper" id="hs-cta-wrapper-a9ef4604-6380-4301-8e92-05720f825642"><span class="hs-cta-node hs-cta-a9ef4604-6380-4301-8e92-05720f825642" id="hs-cta-a9ef4604-6380-4301-8e92-05720f825642"><!--[if lte IE 8]><div id="hs-cta-ie-element"></div><![endif]--><a href="https://cta-redirect.hubspot.com/cta/redirect/2832298/a9ef4604-6380-4301-8e92-05720f825642" rel="noopener" target="_blank"><img alt="Get Inside Real AI Network Flows" class="hs-cta-img" id="hs-cta-img-a9ef4604-6380-4301-8e92-05720f825642" src="https://no-cache.hubspot.com/cta/default/2832298/a9ef4604-6380-4301-8e92-05720f825642.png" style="border-width: 0px;" /></a></span></span><!-- end HubSpot Call-to-Action Code -->
</div>



<h2 class="wp-block-heading">AI: The elephant in the room</h2>



<p>AI workflows don’t just need a place to store data, they need to be able to move it <a href="https://www.backblaze.com/blog/point-to-point-at-100gbps-what-ai-grade-infrastructure-actually-requires/" rel="noreferrer noopener" target="_blank">quickly, easily, and nearly constantly for short bursts</a>. Large, multi-petabyte datasets are ingested, transformed, exported for training, pulled back for evaluation, and periodically refreshed as models evolve.  </p>



<p>Backblaze plays a key role at both ends of that lifecycle. We serve as a durable storage layer for the initial data ingestion, and as the high-throughput source feeding model training, evaluation, and validation to whatever best neocloud is suitable at the moment. Once that model has been trained, it needs to be stored, served, and periodically retrained, where we serve as the storage medium.</p>



<p>From a network perspective, this represents a meaningful shift from diffuse, internet-style traffic patterns to large, high-bandwidth flows between a smaller set of endpoints typical of AI-centric infrastructure.</p>



<h2 class="wp-block-heading">Trends and spring renewal</h2>



<p>The defining theme of the quarter is “winter freeze” as we observed what looks to be a quiet period of Neocloud and hyperscaler traffic over the winter months with an uptick in March.&nbsp;</p>



<p>The stacked area graph below shows total traffic by network type over time updated with the most current data. Hosting and internet service provider (ISP) traffic stayed largely within historical norms reflecting steady-state usage patterns. Three slices stand out this quarter:</p>



<ul class="wp-block-list">
<li><strong>CDN traffic</strong>: Increase in CDN traffic over the winter months.</li>



<li><strong>Neocloud traffic: </strong>After the October 2025 peak, we saw a decline in neocloud traffic heading into January. The winter months were a low volume period with an upward trend observed February into March 2026.</li>



<li><strong>Hyperscaler traffic</strong>: Hyperscaler traffic also followed the Neocloud pattern of a low period during winter with an upward trend in March 2026.</li>
</ul>


<div class="wp-block-image">
<figure class="aligncenter size-large wp-lightbox-container"><img alt="A chart showing Backblaze network traffic for Q1 2026." class="wp-image-112960" height="597" src="https://backblaze.com/blog/wp-content/uploads/2026/04/2026-q1_stacked_area_chart_network_type-1024x597.png" width="1024" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button><figcaption class="wp-element-caption">Monthly view of all bits transferred to each network type (2025-05 to current)</figcaption></figure>
</div>


<div class="wp-block-spacer" style="height: 10px;"></div>



<p>With more than three quarters of data at our disposal, we can now start to see some trends over time. What do we think is happening?&nbsp;</p>



<p>This could be an indication of the human element where the business cycle has a lot of downtime in the winter months—all of our code, infrastructure, computing jobs, and new innovations involve people somewhere along the chain and we all (hopefully) tend to take more time off in the winter months.</p>



<p>Another hypothesis is that our numbers only show bits transferred over our network links over time. If a large dataset has been stored with us, there may not need to be an update to the large stored dataset for a number of months as code and models are refined, and then suddenly a large amount of new data makes its way over our network links. Perhaps a combination of both—human and training lifecycle?</p>



<p>We’ll be tracking these metrics and updating in future reports, so this high-level view of network traffic segmented by network type will be interesting to watch.</p>



<h2 class="wp-block-heading">Chart overview</h2>



<p>Now let’s take a deep dive into our data and answer these questions:</p>



<ul class="wp-block-list">
<li><a href="#q-o-q-heatmaps">Quarter over quarter heatmaps</a>
<ul class="wp-block-list">
<li><a href="#heatmap-1-location" id="#heatmap-1-location" type="internal">Where did we send and receive the most traffic?</a></li>



<li><a href="#heatmap-2-magnitude" id="#heatmap-2-magnitude" type="internal">Where were the data transfers with the most magnitude (bits per IP address)?</a></li>



<li><a href="#heatmap-3-unique-IPs" id="#heatmap-3-unique-IPs" type="internal">How many unique addresses do we interact with?</a></li>
</ul>
</li>



<li><a href="http://traffic-summary">Traffic flow summary</a></li>



<li><a href="#neocloud-geography" id="#neocloud-geography" type="internal">Geographical heatmaps</a>: Where in the world is the neocloud? 
<ul class="wp-block-list">
<li><a href="#neocloud-heatmap-1-countries" id="#neocloud-heatmap-1-countries" type="internal">What countries show the highest concentration of traffic by network type?</a></li>



<li><a href="#neocloud-heatmap-2-countriesxUS" id="#neocloud-heatmap-2-countriesxUS" type="internal"> If we exclude the US, what countries show the highest concentration of traffic by network type?</a></li>



<li><a href="#neocloud-heatmap3-US-states" id="#neocloud-heatmap3-US-states" type="internal">Which U.S. States show the highest concentration of traffic by network type?</a></li>
</ul>
</li>



<li><a href="#neocloud-hyperscale-patterns" id="#neocloud-hyperscale-patterns" type="internal">Traffic dynamics over time</a>
<ul class="wp-block-list">
<li><a href="#neocloud-hyperscaler-time" id="#neocloud-hyperscaler-time" type="internal">What’s the magnitude of neocloud and hyperscaler traffic over time?</a></li>



<li><a href="#neocloud-hyperscaler-heatmaps" id="#neocloud-hyperscaler-heatmaps" type="internal">How dynamic are neocloud and hyperscaler traffic patterns?  </a></li>



<li><a href="#CDN-hosting-ISP-dynamic">How dynamic are CDN, hosting, and ISP regional traffic patterns?</a></li>
</ul>
</li>
</ul>



<h2 class="wp-block-heading" id="q-o-q-heatmaps">Quarter over quarter heatmaps: How and where data moves</h2>



<p>To better understand our network activity, we isolated variables like region and types of provider. Let’s look at the following dimensions:&nbsp;</p>



<ol class="wp-block-list">
<li><strong>Total traffic volume:</strong> Where did we send and receive the most traffic? </li>



<li><strong>Magnitude:</strong> Where were the data transfers with the most bits per unique IP address?</li>



<li><strong>Uniqueness:</strong> What does the number of distinct IP addresses look like? </li>
</ol>



<div class="wp-block-group has-background" style="background-color: #f5f4ff;"><div class="wp-block-group__inner-container is-layout-constrained wp-block-group-is-layout-constrained">
<p>Quick terminology refresher</p>



<ul class="wp-block-list">
<li>Regions
<ul class="wp-block-list">
<li>US-West: Our largest and longest-running region</li>



<li>US-East: Region with the most observed proximity to neocloud infrastructure</li>



<li>CA-East: Our newest region in Canada. </li>
</ul>
</li>



<li>Network Types
<ul class="wp-block-list">
<li>CDN: Networks that use Backblaze as an origin store for content delivery </li>



<li>Hosting: Traditional hosting providers that runs workloads like physical or virtual servers for web, database, or application tasks</li>



<li>Hyperscaler: Large, traditional cloud providers</li>



<li>ISP Regional: Local or regional ISPs, think of these as the “last mile” paths as these networks are very close to customer equipment and efficient </li>



<li>ISP Tier1: National or international ISPs that carry our traffic long distances</li>



<li>Neocloud: AI -focused compute networks</li>
</ul>
</li>
</ul>
</div></div>



<div class="wp-block-spacer" style="height: 10px;"></div>



<h3 class="wp-block-heading" id="heatmap-1-location">Heatmap #1: Where did we send and receive the most traffic?</h3>



<p>US-West <img alt="↔" class="wp-smiley" src="https://s.w.org/images/core/emoji/17.0.2/72x72/2194.png" style="height: 1em;" /> ISP-Regional traffic continues to be a hotspot on the heatmap, as expected. This region has the largest footprint behind it and connections to internet exchanges (IX). This quarter, with a lull in neocloud and hyperscaler traffic over the winter period, we saw an increase in traffic to our CDN partners. The amount of traffic to CDN networks in the US-West, US-East, and EU-Central regions all increased quarter over quarter.</p>


<div class="wp-block-image">
<figure class="aligncenter size-full wp-lightbox-container"><img alt="Total number of bits transferred across regions in Q1 2026." class="wp-image-112957" height="500" src="https://backblaze.com/blog/wp-content/uploads/2026/04/2026-q1_heatmap_bits_95th.png" width="1000" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button><figcaption class="wp-element-caption">Total number of bits transferred across our regions to each network type for Q1 2026. </figcaption></figure>
</div>


<div class="wp-block-spacer" style="height: 10px;"></div>


<div class="wp-block-image">
<figure class="aligncenter size-large wp-lightbox-container"><img alt="A heatmap showing the total number of bits transferred across network types and by region for Q4 2025." class="wp-image-112750" height="516" src="https://backblaze.com/blog/wp-content/uploads/2026/01/Q4-2025-Network-Stats-Chart-03-1-1024x516.png" width="1024" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button><figcaption class="wp-element-caption">Total number of bits transferred across our regions to each network type in Q4 2025.</figcaption></figure>
</div>


<div class="wp-block-spacer" style="height: 10px;"></div>



<h3 class="wp-block-heading" id="heatmap-2-magnitude">Heatmap #2: Where were the data transfers with the most magnitude (bits per IP address)?</h3>



<p>Another metric we record is bits per IP or what we term “magnitude.” This combination of the amount of traffic transferred with how many actors are involved per network is a good proxy to measure how heavy or impactful individual data flows are. In short:</p>



<ul class="wp-block-list">
<li><strong>High volume, many IPs:</strong> Easier to distribute and load-balance across infrastructure. And many source and destination pairs means that we can traffic engineer at the <a href="https://en.wikipedia.org/wiki/Wide_area_network" rel="noreferrer noopener" target="_blank">WAN</a> layer, sending some traffic over one provider and some over another.</li>



<li><strong>High volume, few IPs: </strong>More difficult, but more interesting, from a NetEng perspective. </li>
</ul>



<p>Despite the total amount of traffic decreasing over the winter months for neocloud traffic, the magnitude of neocloud transfers still remains high. This speaks to the nature of the traffic pattern—when a GPU/compute cluster is ingesting or producing data, it does so at a high bitrate with just a few number of unique endpoints talking to each other.</p>



<p>As expected, the concentration of our magnitude metric is high for our US-East cluster, with an uptick in concentration in US-West and EU-Central. Where specifically is this new concentration in these regions? Spoiler: We explore neocloud traffic later in the report with geographical data!</p>


<div class="wp-block-image">
<figure class="aligncenter size-full wp-lightbox-container"><img alt="A heatmap showing magnitude (bits transferred per IP address) moved across our regions to each network type Q1 2026." class="wp-image-112958" height="500" src="https://backblaze.com/blog/wp-content/uploads/2026/04/2026-q1_heatmap_bits_ip_95th.png" width="1000" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button><figcaption class="wp-element-caption">Magnitude transferred across our regions to each network type for Q1 2026.</figcaption></figure>
</div>


<div class="wp-block-spacer" style="height: 10px;"></div>


<div class="wp-block-image">
<figure class="aligncenter size-large wp-lightbox-container"><img alt="A chart showing the concentration of bits transferred by IP address and by region for Q4 2025." class="wp-image-112752" height="512" src="https://backblaze.com/blog/wp-content/uploads/2026/01/Q4-2025-Network-Stats-Chart-04-1024x512.png" width="1024" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button><figcaption class="wp-element-caption">Magnitude transferred across our regions to each network type for Q4 2025.</figcaption></figure>
</div>


<div class="wp-block-spacer" style="height: 10px;"></div>



<p>As with last quarter, we see a high concentration of neoclouds in US-East, but our new heatmap also shows a rising activity in US-West and EU-Central. We also see more distribution in other use cases. </p>



<h3 class="wp-block-heading" id="heatmap-3-unique-IPs">Heatmap #3: How many unique addresses do we interact with?</h3>



<p>Uniqueness—measured by the number of distinct IP addresses per network type—adds another dimension to the story. Unsurprisingly, the quarter over quarter heatmap looks almost identical. This is expected with our US-West region being the most mature and serving a large amount of ISP Regional consumers and is a good sanity check on our dataset.</p>



<ul class="wp-block-list">
<li>US-West shows the highest overall uniqueness, driven by its larger number of data centers and mix of workloads.</li>



<li>Neocloud traffic, by contrast, tends to involve fewer, more persistent endpoints, consistent with AI pipelines that rely on stable, long-standing connections between storage and compute. </li>
</ul>



<p>This is where we can clearly see those AI networking elephant flows showing up in the data.</p>


<div class="wp-block-image">
<figure class="aligncenter size-full wp-lightbox-container"><img alt="A heatmap showing the sum of unique IP addresses by use case and region for Q1 2026." class="wp-image-112959" height="500" src="https://backblaze.com/blog/wp-content/uploads/2026/04/2026-q1_heatmap_ip_unique_95th.png" width="1000" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button><figcaption class="wp-element-caption">Communication uniqueness across our regions to each network type for Q1 2026. </figcaption></figure>
</div>


<div class="wp-block-spacer" style="height: 10px;"></div>


<div class="wp-block-image">
<figure class="aligncenter size-large wp-lightbox-container"><img alt="A chart showing the number of unique IP addresses that sent or received data to the Backblaze networks by region for Q4 2025. " class="wp-image-112753" height="516" src="https://backblaze.com/blog/wp-content/uploads/2026/01/Q4-2025-Network-Stats-Chart-05-1024x516.png" width="1024" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button><figcaption class="wp-element-caption">Communication uniqueness across our regions to each network type for Q4 2025.</figcaption></figure>
</div>


<div class="wp-block-spacer" style="height: 10px;"></div>



<h3 class="wp-block-heading" id="traffic-summary">Summary: Seasonal change in traffic flows</h3>



<p>With a lull in bits transferred as noted in our top level graph, we can see what other networks by percentage took over. CDN traffic increased from around 20% to 32% of our total traffic, localized ISP regional traffic also increased 21.5% to 27.8%. Neocloud and hyperscaler traffic reduced from 36.4% in Q4 2025 to 25.5% in Q1 2026. </p>



<h2 class="wp-block-heading">Quarter over quarter data</h2>



<p>We’re tracking our usual metrics here, and we gave you both this quarter and last quarter’s charts so you can easily spot potential trends.&nbsp;&nbsp;</p>



<p>First let’s take a look at where all our traffic goes from a global perspective with an updated view of last quarter.</p>


<div class="wp-block-image">
<figure class="aligncenter size-large wp-lightbox-container"><img alt="A sankey diagram of all ingress and egress traffic grouped by type of network for Q1 2026. " class="wp-image-112961" height="754" src="https://backblaze.com/blog/wp-content/uploads/2026/04/2026-q1_total_traffic-1024x754.png" width="1024" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button><figcaption class="wp-element-caption">A Sankey diagram of all ingress and egress traffic grouped by type of network for Q1 2026. </figcaption></figure>
</div>


<div class="wp-block-spacer" style="height: 10px;"></div>


<div class="wp-block-image">
<figure class="aligncenter size-large wp-lightbox-container"><img alt="A Sankey diagram that tracks total data traffic flow between Backblaze and different types providers for Q4 2025." class="wp-image-112754" height="767" src="https://backblaze.com/blog/wp-content/uploads/2026/01/Q4-2025-Network-Stats-Chart-06-1024x767.png" width="1024" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button><figcaption class="wp-element-caption">A Sankey diagram of all ingress and egress traffic grouped by type of network for Q4 2025. </figcaption></figure>
</div>


<div class="wp-block-spacer" style="height: 10px;"></div>



<p>Next, let’s take a look at the geography of our network traffic. As we’ve already seen in previous heatmaps, data gravity is concentrating traffic into specific locations.</p>



<h2 class="wp-block-heading" id="neocloud-geography">Where in the world is the neocloud? </h2>



<p>New for March 2026, we’ve added geographic information to our dataset, allowing us to take a look at the concentration of traffic based on network types. We’re taking a look into the following locational slices:</p>



<ol class="wp-block-list">
<li>Countries</li>



<li>Countries excluding the United States</li>



<li>U.S. states</li>
</ol>



<h3 class="wp-block-heading" id="neocloud-heatmap-1-countries">Heatmap #1: What countries show the highest concentration of traffic by network type?</h3>



<p>Neocloud, hyperscaler, and CDN traffic in our dataset all show high concentrations in the United States. Is this due to our US-West and US-East regions being the largest of our deployments or is it related to how certain traffic types are present in the emerging AI market? A quick search shows that the U.S. contains around 40-45% of all data centers globally, so it’s likely the sheer deployment size and scope of US sites aligns with what we’re seeing at the network level.</p>


<div class="wp-block-image">
<figure class="aligncenter size-large wp-lightbox-container"><img alt="Total number of bits transferred by network type to countries from March 2026. 
" class="wp-image-112949" height="384" src="https://backblaze.com/blog/wp-content/uploads/2026/04/2026-03_heatmap_types_top20_country-1024x384.png" width="1024" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button><figcaption class="wp-element-caption">Total number of bits transferred by network type to countries from March 2026. </figcaption></figure>
</div>


<div class="wp-block-spacer" style="height: 10px;"></div>



<p>That said, excluding outliers can show us additional geographic trends, which leads to our next heatmap.</p>



<h3 class="wp-block-heading" id="neocloud-heatmap-2-countriesxUS">Heatmap #2: If we exclude the U.S., what countries show the highest concentration of traffic by network type?</h3>



<p>Since the United States numbers highly skew the heatmap concentration, below is a heatmap without the US to give us better fidelity on ex-US datapoints. Interesting to note that we deliver a large amount of traffic to CDN entities in the Netherlands. This is due in part to our connectivity to <a href="https://www.ams-ix.net/ams" rel="noreferrer noopener" target="_blank">AMS-IX</a> (Amsterdam Internet Exchange). </p>



<p>The network posture of Europe differs from the United States to where local IX networks are preferred over larger Tier1 ISP networks for transit (politically, cost, and preference wise). Second up is Singapore for CDN content and hosting activity in Germany. The next standout is a concentration of neocloud related activity in Finland, Brazil, France, and Canada.</p>


<div class="wp-block-image">
<figure class="aligncenter size-large wp-lightbox-container"><img alt="Total number of bits transferred by network type to countries, excluding the United States, from March 2026. " class="wp-image-112948" height="384" src="https://backblaze.com/blog/wp-content/uploads/2026/04/2026-03_heatmap_types_top20_country-ex-us-1024x384.png" width="1024" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button><figcaption class="wp-element-caption">Total number of bits transferred by network type to countries, excluding the United States, from March 2026. </figcaption></figure>
</div>


<div class="wp-block-spacer" style="height: 10px;"></div>



<h3 class="wp-block-heading" id="neocloud-heatmap3-US-states">Heatmap #3: What U.S. States show the highest concentration of traffic by network type?</h3>



<p>If we dive into just the U.S. States, we can see the heavily weighted concentration of neocloud traffic to and from California. Hyperscaler activity matching up with our expectations as California and Virginia (specifically the Ashburn and Reston corridor) have a high concentration of partner networks. CDN traffic for us concentrates more for Backblaze specifically since the US-West region is our largest cluster footprint and longest running sites, so naturally the data being served out of these sites is more long-lived content lifecycle wise.</p>


<div class="wp-block-image">
<figure class="aligncenter size-large wp-lightbox-container"><img alt="Total number of bits transferred by network type to US States from March 2026. " class="wp-image-112950" height="384" src="https://backblaze.com/blog/wp-content/uploads/2026/04/2026-03_heatmap_types_top20_us_states-1024x384.png" width="1024" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button><figcaption class="wp-element-caption">Total number of bits transferred by network type to US States from March 2026. </figcaption></figure>
</div>


<div class="wp-block-spacer" style="height: 10px;"></div>



<p>These insights into data geography help us understand, plan, and modify our growth trajectory. I say “help,” because we’re also discovering that neocloud and hyperscaler activity is very bursty and has a high magnitude of traffic flow below. From a planning perspective, understanding whether those bursts translate to a higher baseline for increased demand—and how to support bursts when they happen—is a different conversation than the predictable network trends of years past. </p>



<h2 class="wp-block-heading" id="neocloud-hyperscale-patterns">Neocloud and hyperscaler traffic vs predictive patterns</h2>



<p>This quarter we’re sharing a deeper dive into the metrics associated with neocloud and hyperscalers over time. These two traffic types are driving innovation at Backblaze and are interesting to share to the larger industry. While CDN, hosting, and ISP regional traffic patterns are easy for us to model and account for as we manage our network infrastructure, neocloud and hyperscalers growth profiling are a challenge! As we said above, they are bursty and have a high magnitude (bits per associated IP address).</p>



<p>And, in the spirit of that conversation, we have several new views to share:</p>



<ul class="wp-block-list">
<li>Neocloud and hyperscaler magnitude (bits per IP address) over time</li>



<li>Heatmaps over time
<ul class="wp-block-list">
<li>Neocloud</li>



<li>Hyperscaler</li>



<li>CDN</li>



<li>Hosting</li>



<li>ISP regional</li>
</ul>
</li>
</ul>



<h3 class="wp-block-heading" id="neocloud-hyperscaler-time">Chart #1: What’s the magnitude of neocloud and hyperscaler traffic over time?</h3>



<p>Matching our earlier charts, we saw a burst of activity from August to December of last year with a resurgence of high magnitude neocloud traffic in March of 2026.</p>


<div class="wp-block-image">
<figure class="aligncenter size-full wp-lightbox-container"><img alt="Magnitude of neocloud and hyperscaler related traffic over time" class="wp-image-112956" height="600" src="https://backblaze.com/blog/wp-content/uploads/2026/04/2026-q1_general_magnitude_by_month.png" width="1000" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button><figcaption class="wp-element-caption">Magnitude of neocloud and hyperscaler related traffic over time. </figcaption></figure>
</div>


<div class="wp-block-spacer" style="height: 15px;"></div>



<h3 class="wp-block-heading" id="neocloud-hyperscaler-heatmaps">Heatmap #1 and #2: How dynamic are neocloud and hyperscaler traffic patterns?</h3>



<p>Neocloud and hyperscaler traffic patterns are the most impactful to our operations due to the magnitude of their data flows. Below is a more detailed look at these concentrations over time, with a burst of activity from August to November for Neoclouds, a quiet period over the winter months, and a pickup again in March.&nbsp;</p>



<p>As expected our US-East region remains a hotspot of Neocloud related activity. One standout from this analysis is that the Neocloud activity in March is more spread out over our US-West, US-East, and EU-Central regions. It will be interesting to see if this spread grows or contracts over time.</p>


<div class="wp-block-image">
<figure class="aligncenter size-full wp-lightbox-container"><img alt="Neocloud monthly traffic totals by region for May 2025–March 2026. " class="wp-image-112955" height="400" src="https://backblaze.com/blog/wp-content/uploads/2026/04/2026-q1_bits_heatmap_neocloud.png" width="1000" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button><figcaption class="wp-element-caption">Neocloud monthly traffic totals by region for May 2025–March 2026. </figcaption></figure>
</div>


<div class="wp-block-spacer" style="height: 10px;"></div>



<p>Over the winter months, there was a noticeable decrease in activity for hyperscale related traffic, most notable in January, but when compared to neocloud traffic, the month-over-month traffic patterns remained strongly visible in our US-East region.</p>


<div class="wp-block-image">
<figure class="aligncenter size-full wp-lightbox-container"><img alt="Hyperscaler monthly traffic totals by region for May 2025–March 2026. " class="wp-image-112953" height="400" src="https://backblaze.com/blog/wp-content/uploads/2026/04/2026-q1_bits_heatmap_hyperscaler.png" width="1000" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button><figcaption class="wp-element-caption">Hyperscaler monthly traffic totals by region for May 2025–March 2026.</figcaption></figure>
</div>


<div class="wp-block-spacer" style="height: 15px;"></div>



<h3 class="wp-block-heading" id="CDN-hosting-ISP-dynamic">Heatmap #3, #4, and #5: How dynamic are CDN, hosting, and ISP regional traffic patterns?</h3>



<p>We’re grouping CDN, hosting, and ISP regional types together because they represent a “steady-state” for us as network operators. These patterns are predictable, spread out over time, and generally do not change month-to-month. We do see visible bursts of traffic, like with a heavy blue tile for CDN in September and a few areas of hosting related traffic in May and October of 2025, but overall these are less impactful to our operations because the magnitude (bits per unique IP address) is lower—many sources are talking to many destinations, which as operators is easy to load balance.</p>


<div class="wp-block-image">
<figure class="aligncenter size-full wp-lightbox-container"><img alt="CDN monthly traffic totals by region from May 2025–March 2026." class="wp-image-112951" height="400" src="https://backblaze.com/blog/wp-content/uploads/2026/04/2026-q1_bits_heatmap_cdn.png" width="1000" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button><figcaption class="wp-element-caption">CDN monthly traffic totals by region from May 2025–March 2026.</figcaption></figure>
</div>


<div class="wp-block-spacer" style="height: 10px;"></div>


<div class="wp-block-image">
<figure class="aligncenter size-full wp-lightbox-container"><img alt="Hosting monthly traffic totals by region for March 2025–May 2026. " class="wp-image-112952" height="400" src="https://backblaze.com/blog/wp-content/uploads/2026/04/2026-q1_bits_heatmap_hosting.png" width="1000" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button><figcaption class="wp-element-caption">Hosting monthly traffic totals by region for March 2025–May 2026. </figcaption></figure>
</div>


<div class="wp-block-spacer" style="height: 10px;"></div>


<div class="wp-block-image">
<figure class="aligncenter size-full wp-lightbox-container"><img alt="ISP Regional monthly traffic totals by region for March 2025–May 2026." class="wp-image-112954" height="400" src="https://backblaze.com/blog/wp-content/uploads/2026/04/2026-q1_bits_heatmap_isp-regional.png" width="1000" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button><figcaption class="wp-element-caption">ISP Regional monthly traffic totals by region for March 2025–May 2026.</figcaption></figure>
</div>


<div class="wp-block-spacer" style="height: 10px;"></div>



<p>The most striking example of this predictability is, unsurprisingly, ISP regional traffic. This represents your more consumer driven workflows and use cases.</p>



<h2 class="wp-block-heading">Neocloud business cycle and geography</h2>



<p>We can draw a conclusion from all these charts: neocloud and hyperscaler are both different traffic patterns and far more dynamic than CDN, hosting, and ISP regional traffic. For our Network Engineering group, this means we have two different stylistic approaches towards managing our network.&nbsp;</p>



<p>First, when planning for the neocloud and hyperscaler traffic, our solutions entail adding large amounts of additional bandwidth in increments of 100G and often 400G ports to handle burst rates, ensuring that our inter-switch links inside our datacenter can also handle bursts of traffic, and reaching out to select partners to establish <a href="https://en.wikipedia.org/wiki/Private_Network-to-Network_Interface">private network-to-network interface (PNI) connections</a> where appropriate for zero-settlement transit.&nbsp;</p>



<p>Our steady state growth patterns stem from CDN, hosting, and ISP regional traffic with easy to model growth curves. Looking over monthly numbers indicates a clear pattern for us, and that’s easy to plan for.</p>



<p>The last factor that we’re placing more emphasis on is the geographical location of our network interconnections. We’re seeing a high concentration of demand located in the United States, specifically in regions like California, Virginia, Illinois, and Georgia.</p>



<p>With more datapoints, we can clearly see the magnitude of the neocloud and hyperscaler transfers when compared to other network types. As above, it’s a bit early to claim concrete quarter over quarter patterns, but we’ll keep monitoring and updating the dataset.&nbsp;</p>



<h2 class="wp-block-heading">What’s next?</h2>



<p>Anything specific you want to see? Let us know in the comments or reach out to the <a href="mailto:drivestats@backblaze.com">Network Stats team</a>. Or, keep up-to-date with the latest technical content with our <a href="https://info.backblaze.com/tech-community-sign-up?portalId=2832298&amp;hsCtaTracking=665870a9-b08d-4b9e-8653-722affcd5124%7Ca0cea694-ef1b-4736-931e-5fd240300619" rel="noreferrer noopener" target="_blank">Developer Newsletter.</a> <br /></p>
<p>The post <a href="https://www.backblaze.com/blog/network-stats-for-q1-2026-neocloud-traffic-trends/">Network Stats for Q1 2026: Neocloud Traffic Trends</a> appeared first on <a href="https://www.backblaze.com/blog">Backblaze Blog | Cloud Storage &amp; Cloud Backup</a></p>
