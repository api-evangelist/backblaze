---
title: "Point-to-Point at 100Gbps: What AI-Grade Infrastructure Actually Requires"
url: "https://www.backblaze.com/blog/point-to-point-at-100gbps-what-ai-grade-infrastructure-actually-requires/"
date: "Thu, 23 Apr 2026 17:00:01 +0000"
author: "Brent Nowak"
feed_url: "https://www.backblaze.com/blog/feed/"
---
<figure class="wp-block-image size-full"><img alt="A decorative image that shows several cubes on a background. " class="wp-image-112938" height="820" src="https://backblaze.com/blog/wp-content/uploads/2026/04/Q126-0005-Blog-Header-1440x820-1.png" width="1440" /></figure>



<div class="wp-block-spacer" style="height: 15px;"></div>



<p>Bandwidth purchased for data center connectivity surged by nearly 330% between 2020 and 2024, driven primarily by AI workloads. And in 2024, just 10 buyers accounted for nearly 62% of all purchases, according to <a href="https://www.datacenterknowledge.com/networking/data-center-bandwidth-soars-330-driven-by-ai-demand" rel="noreferrer noopener" target="_blank">Zayo&#8217;s Bandwidth Report</a>. That concentration is a structural feature of how AI moves data.</p>



<p>Every training run that pulls data from Backblaze storage to a neocloud passes through our network, and our <a href="https://www.backblaze.com/blog/tag/networkstats/" rel="noreferrer noopener" target="_blank">telemetry</a> captures what those flows look like in real time. Our <a href="https://www.backblaze.com/blog/network-stats-for-q4-2025-neocloud-traffic-trends/" rel="noreferrer noopener" target="_blank">Q4 2025 Network Stats</a> report covers a full quarter of that data. It shows AI workloads producing a distinct network signature: sustained, high-volume transfers between a small number of endpoints, with infrastructure requirements specific enough to be worth examining in detail.</p>



<p>This piece walks through what that signature looks like and what it means for the infrastructure decisions teams are making right now.</p>



<h2 class="wp-block-heading">The AI model lifecycle and how it moves data</h2>



<p>AI model development is a cycle. Large datasets are ingested and consolidated, exported to compute for training, pulled back for evaluation, then pushed out again as models are refined, retrained, and updated with new data. Each stage requires moving substantial volumes of data between <a href="https://www.backblaze.com/blog/architecting-your-ai-data-pipeline-using-b2-overdrive/" rel="noreferrer noopener" target="_blank">storage and compute, repeatedly, over the life of a model.</a></p>



<figure class="wp-block-image size-full wp-lightbox-container"><img alt="A workflow diagram showing the different aspects of the storage layer for AI. " class="wp-image-112939" height="490" src="https://backblaze.com/blog/wp-content/uploads/2026/04/1_Backblaze_Storage-layer-AI.png" width="936" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button></figure>



<div class="wp-block-spacer" style="height: 10px;"></div>



<p>That structure produces a specific kind of network traffic. AI training moves petabyte-scale data between storage and compute nodes in sustained, long-lived flows—what network engineers call <a href="https://en.wikipedia.org/wiki/Elephant_flow" rel="noreferrer noopener" target="_blank">elephant flows</a>—with training jobs running for hours or days under continuous network load. Add frequent checkpointing, model updates, and periodic data refreshes, and the result is traffic that is high in volume and persistent across the entire training run.</p>



<p>This shows up clearly in the <a href="https://www.backblaze.com/blog/network-stats-for-q4-2025-neocloud-traffic-trends/" rel="noreferrer noopener" target="_blank">Q4 2025 Network Stats data</a>. Neocloud traffic spiked sharply from July through November, peaking in October, then settled into a higher baseline heading into the new year. One interpretation of that shape is the AI lifecycle playing out across a concentration of large training cycles: ingestion, training egress, then a new steady state as stored models get served and periodically retrained. As we accumulate more quarters of data across a broader customer mix, we&#8217;ll be better positioned to distinguish that pattern from seasonal budget cycles or customer-specific factors.</p>


<div class="wp-block-image">
<figure class="aligncenter size-full wp-lightbox-container"><img alt="A chart showing Backblaze network traffic for Q4 2025. " class="wp-image-112940" height="546" src="https://backblaze.com/blog/wp-content/uploads/2026/04/2_Backblaze_Networking-flow.png" width="936" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button><figcaption class="wp-element-caption">Backblaze network traffic for Q4 2025. </figcaption></figure>
</div>


<div class="wp-block-spacer" style="height: 10px;"></div>



<p>Also visible in the Q4 data is where this traffic is going. Cloud-to-cloud traffic grew from 36.2% to 49.6% quarter-over-quarter, with hyperscaler destinations rising from 3.5% to 18%. As the report notes, it&#8217;s too early to call these statistically significant trends; the dataset reflects Backblaze&#8217;s specific customer mix and covers a single quarter. The direction is consistent with how AI teams operate in practice: moving workloads across neoclouds and hyperscalers depending on price, availability, and job requirements. The storage layer is what persists across those compute environments, which has direct implications for how it needs to be designed.</p>



<h2 class="wp-block-heading">What elephant flows require from a network</h2>



<p>Traditional cloud infrastructure is designed around a specific traffic profile: many clients, many sessions, many discrete transactions. Routing, <a href="https://www.backblaze.com/blog/load-balancing-2-0-whats-changed-after-7-years/" rel="noreferrer noopener" target="_blank">load balancing</a>, and edge capacity are all optimized for that pattern, distributing load broadly and handling high volumes of short-lived connections efficiently.</p>



<p>Elephant flows don&#8217;t fit that profile. AI training establishes persistent, high-volume connections between client and storage that sustain continuous data movement for hours or days at a time. These connections are stickier than typical cloud traffic, particularly on peered networks, and the strain they produce is concentrated rather than distributed—showing up primarily at the edge, where routers handle sustained throughput at scale. Most traditional cloud infrastructure wasn&#8217;t provisioned for that kind of sustained pressure at the edge, because most workloads don&#8217;t produce it. Internal to the network, depending on a myriad of things—object size, concurrent threads, hardware, internal routing logic—your network path being sticky doesn’t reduce the number of <a href="https://www.backblaze.com/blog/one-simple-change-that-made-our-exabyte-scale-storage-faster/" rel="noreferrer noopener" target="_blank">I/O operations</a> for servers, and often that becomes one of the biggest bottlenecks. </p>



<p>The stakes make this consequential. Training the most advanced models now costs hundreds of millions of dollars, according to <a href="https://epoch.ai/data-insights/cost-trend-large-scale" rel="noreferrer noopener" target="_blank">Epoch AI</a>—though we also know this is a new technology, and therefore likely the compute will get <a href="https://arstechnica.com/ai/2026/03/google-says-new-turboquant-compression-can-lower-ai-memory-usage-without-sacrificing-quality/#:~:text=Even%20if%20you%20don't,run%20them%20at%20lower%20precision" rel="noreferrer noopener" target="_blank">more efficient over time</a>. That said, the <a href="https://www.backblaze.com/cloud-storage/b2-overdrive" rel="noreferrer noopener" target="_blank">storage</a> is still storage: Data has to live somewhere.  </p>



<p>Infrastructure that can&#8217;t sustain throughput under continuous load doesn&#8217;t just slow training down; it adds cost to every run. The practical answer is building throughput capacity at the connection points between storage infrastructure and the internet or peer network, sized for sustained flows rather than peak bursts.</p>



<p>That&#8217;s what AI-grade storage infrastructure is designed around: sustained throughput to a small number of destinations, at 100Gbps to 1Tbps per transfer for the largest AI workflows. Achieving that in practice means rethinking how a network is designed, routed, and scaled. <a href="https://www.backblaze.com/blog/making-the-backblaze-network-ai-ready/" rel="noreferrer noopener" target="_blank">We&#8217;ve written separately about what that looked like for Backblaze&#8217;s own infrastructure</a>. Latency matters here for a specific reason: on long-distance transfers, higher latency directly limits achievable sustained throughput, which is one reason why geographic proximity to compute infrastructure affects real-world performance. </p>



<p>The Q4 Network Stats heatmaps show this pattern from two angles. The magnitude heatmap, measuring bits transferred per unique IP address, shows high-magnitude neocloud flows clustering clearly in regions serving AI-heavy compute endpoints. The uniqueness heatmap shows neocloud traffic involving fewer, more persistent endpoints than CDN or ISP traffic, consistent with AI pipelines that rely on stable, long-standing connections between storage and compute.</p>



<h2 class="wp-block-heading">The geography of AI infrastructure</h2>



<p>The heatmaps show where AI traffic concentrates geographically today. Neocloud activity in the Q4 dataset clusters in Chicago, Dallas-Houston, Denver, New York, the Northern Virginia Reston/Ashburn corridor, and Atlanta, with a clear skew toward the East Coast. This reflects where AI compute infrastructure was built first and remains densest. Keeping latency low between storage and compute is a prerequisite for sustaining the high throughput rates AI workflows require, and that constraint has historically made East Coast proximity an advantage.</p>


<div class="wp-block-image">
<figure class="aligncenter size-full wp-lightbox-container"><img alt="A heatmap showing the bits transferred to unique IP addresses by network type and region in Q4 2025. " class="wp-image-112941" height="468" src="https://backblaze.com/blog/wp-content/uploads/2026/04/3_Backblaze_Networking-heat-map.png" width="936" /><button class="lightbox-trigger" type="button">
			<svg fill="none" height="12" viewBox="0 0 12 12" width="12" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 0a2 2 0 0 0-2 2v2h1.5V2a.5.5 0 0 1 .5-.5h2V0H2Zm2 10.5H2a.5.5 0 0 1-.5-.5V8H0v2a2 2 0 0 0 2 2h2v-1.5ZM8 12v-1.5h2a.5.5 0 0 0 .5-.5V8H12v2a2 2 0 0 1-2 2H8Zm2-12a2 2 0 0 1 2 2v2h-1.5V2a.5.5 0 0 0-.5-.5H8V0h2Z" fill="#fff">
			</svg>
		</button><figcaption class="wp-element-caption">Magnitude transferred across our regions to each network type in Q4 2025. </figcaption></figure>
</div>


<div class="wp-block-spacer" style="height: 10px;"></div>



<p>That concentration is consistent with broader infrastructure dynamics. AI training workloads are driving demand for regions with available power, fiber density, and compute infrastructure, and power constraints in preferred markets are already forcing operators to explore secondary locations and invest in custom power infrastructure. Demand in markets outside traditional data center hubs is growing rapidly as a result: <a href="https://www.datacenterknowledge.com/networking/data-center-bandwidth-soars-330-driven-by-ai-demand" rel="noreferrer noopener" target="_blank">Metro bandwidth in Memphis grew from 0.3 terabits to 13.2 terabits between 2023 and 2024</a>. On the flip side, building out cabling to those traditionally under-utilized locations is expensive, often adding thousands of dollars per month to data center economics. High-capacity interconnects are central to making those secondary locations viable; without them, the compute investment is stranded. </p>



<p>The scale of what&#8217;s being built reflects the trajectory of the workload. AI training infrastructure is projected to grow at a 22% compound annual growth rate (CAGR) through 2030, reaching more than 60GW of capacity, while inference infrastructure is expected to grow faster still at 35% CAGR, reaching more than 90GW, <a href="https://www.mckinsey.com/industries/technology-media-and-telecommunications/our-insights/the-next-big-shifts-in-ai-workloads-and-hyperscaler-strategies" rel="noreferrer noopener" target="_blank">according to McKinsey</a>. Training and inference have different geographic requirements: training tolerates latency and can sit in power-rich remote locations, while inference needs to be close to users, which means the buildout will be distributed across both dense metro markets and secondary locations connected by high-capacity fiber.</p>



<p>Backblaze&#8217;s own infrastructure decisions reflect this pattern directly. The East Coast concentration drove the decision to <a href="https://ir.backblaze.com/news/news-details/2025/Backblaze-Fuels-Open-Cloud-Revolution-with-Data-Region-Expansion-Doubling-Down-on-High-Performance-Storage-for-AI-High-Performance-Compute-HPC-and-Media-Workflows/default.aspx" rel="noreferrer noopener" target="_blank">double Backblaze&#8217;s US-East footprint</a>. At 100Gbps and above, proximity to where AI compute is actually running is a determining factor in storage performance.</p>



<h2 class="wp-block-heading">What AI-ready storage infrastructure actually means</h2>



<p>Storage has traditionally been sized for capacity and evaluated on cost per terabyte. <a href="https://www.backblaze.com/blog/neoclouds-are-winning-on-compute-storage-shouldnt-slow-them-down/" rel="noreferrer noopener" target="_blank">AI workflows change the calculus.</a> When a training run is pulling petabytes of data from object storage to flash storage at sustained 100Gbps rates, the storage layer is as much a performance determinant as the compute layer. A storage system that can&#8217;t sustain those throughput rates creates a bottleneck that no amount of GPU capacity can compensate for.</p>



<p>Throughput capability is one requirement. <a href="https://www.backblaze.com/blog/cloud-101-data-egress-fees-explained/" rel="noreferrer noopener" target="_blank">Portability is the other.</a> The multi-cloud behavior visible in the Q4 data reflects how AI teams actually operate: moving workloads to whichever compute provider offers the best price-performance for a given job. Storage that is tightly coupled to one cloud provider is structurally incompatible with that workflow. Data that can&#8217;t <a href="https://www.backblaze.com/blog/escaping-egress-hidden-cloud-fees-every-cfo-should-know/" rel="noreferrer noopener" target="_blank">move freely across cloud environments</a> becomes a constraint on the model development process.</p>



<p>This is the infrastructure problem <a href="https://www.backblaze.com/cloud-storage/b2-overdrive" rel="noreferrer noopener" target="_blank">Backblaze B2 Overdrive</a> is designed to address. By building a direct, high-performance path between Backblaze&#8217;s storage layer and the neoclouds where AI processing takes place, it provides the sustained throughput that training workflows require alongside the portability to move data as compute requirements change. The connections between Backblaze and neocloud endpoints visible in the Q4 heatmaps represent that architecture in practice.</p>



<p>The point extends beyond any single product. As <a href="https://www.backblaze.com/cloud-storage/industries/ai-ml" rel="noreferrer noopener" target="_blank">AI workloads</a> become a larger share of overall data center activity, the criteria for evaluating storage infrastructure are shifting. Capacity and cost per terabyte remain relevant, but sustained throughput capability, interoperability with compute providers, and network proximity to AI infrastructure are becoming equally important factors. Teams that treat storage as a passive component in AI pipeline design are likely to find it becomes the active constraint.</p>



<h2 class="wp-block-heading">Early signal, long trend</h2>



<p>The Q4 2025 <a href="https://www.backblaze.com/blog/tag/networkstats/" rel="noreferrer noopener" target="_blank">Network Stats</a> data is one quarter of observations from one storage provider&#8217;s network. The patterns it shows—high-magnitude flows to a small number of endpoints, East Coast geographic concentration, rising cloud-to-cloud traffic, a higher baseline heading into the new year—are consistent with what the broader industry understands about how AI moves data. What&#8217;s new is that they&#8217;re visible in real network telemetry rather than modeled projections.</p>



<p>We&#8217;ll be watching how neocloud traffic concentration evolves regionally, how the training-to-inference ratio shifts as inference infrastructure scales, and whether the cloud-to-cloud growth visible this quarter continues.</p>



<p>The full dataset, methodology, and visualizations are in the <a href="https://www.backblaze.com/blog/network-stats-for-q4-2025-neocloud-traffic-trends/" rel="noreferrer noopener" target="_blank">Q4 2025 Network Stats report</a>. For background on how we classify and measure network traffic, the <a href="https://www.backblaze.com/blog/network-stats-for-q3-2025-the-magnitude-of-ai-workflows/" rel="noreferrer noopener" target="_blank">Q3 2025 report</a> covers the dataset in detail, and you can follow the whole series <a href="https://www.backblaze.com/blog/tag/networkstats/" rel="noreferrer noopener" target="_blank">here</a>.</p>
<p>The post <a href="https://www.backblaze.com/blog/point-to-point-at-100gbps-what-ai-grade-infrastructure-actually-requires/">Point-to-Point at 100Gbps: What AI-Grade Infrastructure Actually Requires</a> appeared first on <a href="https://www.backblaze.com/blog">Backblaze Blog | Cloud Storage &amp; Cloud Backup</a></p>
