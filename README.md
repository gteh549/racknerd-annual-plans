# USA VPS Hosting: What Does RackNerd Cost Per Year, Will the Renewal Price Jump, and Which Plan Fits Your Workload? (Full Plan Table and Data Center Notes)

RackNerd's current USA VPS specials start at **$11.29 per year** for 1 vCPU, 1 GB RAM, 24 GB SSD and 2 TB of monthly transfer, priced in USD and billed annually rather than monthly. The top of the current lineup is 4 vCPU, 6 GB RAM and 140 GB SSD at **$59.99 per year**. Five plans sit in between, all KVM, all with full root access and a 1 Gbps port.

What follows is the full plan table, what renewal looks like compared with the monthly headline prices other hosts advertise, how to pick a US location, and the point at which a cheap annual box stops being the right purchase.

> Most readers land on one of two plans. The **2 GB plan at $18.29/year** covers a small site, a bot, a VPN endpoint or a staging box. The **3.5 GB plan at $32.49/year** is the first one with room for Docker, a database and a couple of small apps at once. Both are annual prepay. 👉 [See the current RackNerd USA VPS specials](https://bit.ly/RacKnerd)

## The five annual plans, side by side

| Plan | vCPU · RAM · SSD | Transfer (1 Gbps port) | Price (USD, per year) | Order |
| --- | --- | --- | --- | --- |
| Starter | 1 core · 1 GB · 24 GB | 2,000 GB/mo | **$11.29/yr** | [Order Starter](https://bit.ly/RacKnerd) |
| Basic | 1 core · 2 GB · 40 GB | 3,500 GB/mo | **$18.29/yr** | [Order Basic](https://bit.ly/RacKnerd) |
| Popular | 2 cores · 3.5 GB · 65 GB | 7,000 GB/mo | **$32.49/yr** | [Order Popular](https://bit.ly/RacKnerd) |
| Standard | 3 cores · 4 GB · 105 GB | 9,000 GB/mo | **$43.88/yr** | [Order Standard](https://bit.ly/RacKnerd) |
| Power | 4 cores · 6 GB · 140 GB | 12,000 GB/mo | **$59.99/yr** | [Order Power](https://bit.ly/RacKnerd) |

Every plan includes one dedicated IPv4 address, full root SSH access, KVM virtualization and RackNerd's ctrl panel. The specs above are the annual KVM specials as currently listed, and this lineup rotates between promo batches, so check the spec and the price on the order page before you pay rather than assuming the table is frozen.

Three things about the table are worth saying out loud. Storage is SSD, not NVMe, so don't expect NVMe write numbers. The port is 1 Gbps on all five plans, which matters more than the transfer cap for burst traffic. And the price is a yearly figure, not a monthly one dressed up as yearly.

## What the renewal price looks like, and how the monthly headline elsewhere compares

These are annual specials, so the number you see covers twelve months. Third-party reviews of the current batch of RackNerd specials report that renewals stay at the same annual rate rather than jumping, which is unusual enough in this segment to check yourself on the order page before paying. A yearly invoice you can predict beats a monthly headline you can't.

The comparison that matters: Hostinger's US VPS page shows KVM 1 at $6.49/mo with a **$155.76 payment for 24 months**, renewing at $11.99/mo. KVM 4 goes from $12.99/mo to **$28.99/mo** at renewal. KVM 8 goes from $25.99/mo to **$49.99/mo**.

Run KVM 4 forward. The first 24 months cost $311.76. The next 24 months, at the renewal rate, cost **$695.76**. If you keep that server for four years, you pay $1,007.52 for 4 vCPU, 16 GB RAM and 200 GB NVMe, and the discount you clicked on covered less than a third of it. Nothing wrong with the hardware, but the advertised monthly figure is a two-year prepay rate, not a price.

Contabo's US page has its own version of this. The Cloud VPS 18 with 18 vCPU and 96 GB RAM shows **€39.20/mo** marked "for the first 24 months", while a footnote on the same page describes the displayed price as the effective monthly rate for a 12-month subscription. Both statements are on the page and they don't reconcile, so treat that number as a promotional rate with conditions attached and read the cart total before committing. It is also in euros, so don't rank it against dollar prices by the raw digits.

RackNerd's structure is simpler to audit because there is one invoice per year. 👉 [Check the $18.29/year plan and its renewal terms](https://bit.ly/RacKnerd)

## Which US location should you pick?

Location is selected when you order, and it decides your latency more than any spec in the table. RackNerd offers multiple US locations at checkout, and a third-party review of the current specials notes that the Los Angeles DC-02 (Asia-optimized) location is back in stock for the 2 GB plan and above. That last detail matters if part of your audience is in Asia-Pacific rather than North America.

For context on how US hosts spread their footprint: Contabo runs Seattle, St. Louis and Carlstadt, New Jersey, and advertises pings starting at 3 ms across major US metros. Amaze Servers lists New York, Dallas, Chicago, Los Angeles, Atlanta, Miami, Seattle and Silicon Valley. Liquid Web splits between Lansing, Michigan and Phoenix, Arizona. The pattern to copy is regional: east coast for Europe and the eastern seaboard, central for a nationwide average, west for Asia-Pacific traffic.

One decision you cannot undo cheaply. Hostinger states plainly that moving to another data center requires reinstalling the VPS there, which permanently deletes all data including backups and snapshots. Any host that lets you pick a location at checkout has the same physical constraint, RackNerd included, and reinstalling an OS from the ctrl panel wipes the disk. Back up off the box before you experiment, and pick the region you actually need on day one rather than planning to move later.

## What root access actually gets you, and where the 4 GB line falls

RackNerd's specials are unmanaged KVM VPS. You get root over SSH, and the ctrl panel handles power, OS reinstall, an HTML5 VNC console, root password resets, upgrades, an inbound firewall and one-click app installs. Supported installs are CentOS, Rocky Linux, AlmaLinux, Fedora, Debian and Ubuntu, with custom ISO installs available through a support ticket.

The one-click catalog is where plan choice gets concrete. OpenClaw wants at least 8 GB of RAM, which is above the largest plan in the specials table, so that app means a bigger plan than anything listed here. Hermes Agent, AnythingLLM, Ollama and LibreChat want at least 4 GB. n8n and Coolify are comfortable from 2 GB.

That gives you a hard line rather than a vague recommendation: **if you're buying for Ollama, LibreChat, AnythingLLM or Hermes, 4 GB is the floor**, which means Standard at $43.88/year or Power at $59.99/year. The $11.29 and $18.29 plans are for lighter work, and squeezing a 4 GB workload into 2 GB to save $15 a year is how people end up debugging OOM kills at midnight. 👉 [Pick the 4 GB plan for Ollama or a Docker stack](https://bit.ly/RacKnerd)

Two things are not included and are easy to assume. There is no managed service tier here, so patching, hardening and monitoring are yours. And don't assume backups: ctrl's reinstall wipes the disk, so keep a copy somewhere off the server.

## Is the bandwidth unlimited?

No. RackNerd meters it: 2,000 GB, 3,500 GB, 7,000 GB, 9,000 GB and 12,000 GB per month across the five plans, on a 1 Gbps port. For a site doing a few hundred GB a month, or an API handling JSON, none of those caps will come up. Serving video or large downloads will.

Metered is at least honest. Contabo advertises unlimited outgoing traffic but attaches a fair usage policy, stating that it reserves the right to throttle servers with exceptionally high or disruptive usage patterns. IONOS lists unlimited traffic as a feature on its US VPS page without a throttling clause in the section shown. Those are different products with different fine print, and "unlimited" means whatever the policy document says it means. With RackNerd you know the number before you buy, which is the easier thing to plan around.

Watch add-on pricing on any host while you compare. IONOS, for example, charges Cloud Backup from $0.065/GB/month, Plesk at $6/month, additional IPv4 addresses at $5/month each, and domains from $1/year, all on top of the plan price. A cheap base plan with three extras is not a cheap server.

## Who should not buy a RackNerd special

Cheap annual VPS is the wrong purchase in four situations, and it's better to know now than after you've migrated.

**You need HIPAA or SSAE-18 compliance.** Liquid Web's Phoenix data center is SSAE-18 and HIPAA compliant, and its Lansing, Michigan facility is SSAE-18 compliant, with staff on site around the clock. Its US VPS page shows Cloud VPS from $11/mo, memory-optimized from $17/mo and CPU-optimized from $22/mo, with managed options and three support tiers. That page carried a March 2025 date when checked, so treat those as a rough price band rather than today's quote.

**You want someone else to run the server.** RackNerd's specials are self-managed. If you want patching and incident response handled for you, a managed plan is the correct product even at several times the price.

**You need a lot of RAM for very little money.** Contabo's Cloud VPS 18 lists 18 vCPU, 96 GB RAM, 600 GB SSD or 300 GB NVMe and a 1 Gbps port at €39.20/mo under its promotional terms. Nothing in RackNerd's specials table comes close on memory per dollar, and if 96 GB is the requirement, that's the shape of plan you need.

**You need a specific city among many.** Amaze Servers covers eight US metros including Miami, Atlanta and Dallas, with Linux and Windows options and full root. If your users are concentrated in one of those cities and the last few milliseconds matter, more locations is a real feature.

## FAQ

**Does a US VPS actually lower latency for North American visitors?**
Yes, and it's simple physics. Every request travels from the visitor to your server and back, so a server in the US shortens the round trip for US and Canadian users compared with a box in Europe or Asia. Contabo advertises pings from 3 ms within the US on its domestic network, which is the scale of difference a local server buys you.

**Will the price go up at renewal?**
RackNerd sells these as annual specials, and reviews of the current batch report renewals at the same annual rate. Confirm it on the order page for the specific plan before you pay, because promotional batches change.

**Can I move to a different data center after ordering?**
Location is set at deployment. Moving means reinstalling on new hardware, and a reinstall wipes the disk, backups and snapshots included if they live on the same server. Decide the region before you order.

**Is there a fair use throttle on the bandwidth?**
RackNerd publishes a monthly transfer allowance per plan rather than an unlimited figure, so there's no fair-use clause to interpret. You get 2 TB to 12 TB per month depending on the plan, over a 1 Gbps port.

**Can I run Windows?**
Windows isn't among the listed OS options on the specials, which are Linux-first with a choice of CentOS, Rocky, AlmaLinux, Fedora, Debian and Ubuntu. Custom ISO installs can be requested via support ticket, but don't buy expecting a licensed Windows image to be waiting.

**Is it managed?**
No. It's an unmanaged KVM VPS with full root access and a control panel for power, reinstall, console and one-click apps. Support is available around the clock for the platform itself.

## Pick your plan in one line

Running a personal site, a small API, a bot or a VPN endpoint with under 2 GB of working memory? The **$11.29/year Starter** covers it. Want headroom for Docker, a small database and a couple of services? The **$18.29/year Basic** or **$32.49/year Popular** is the sensible ceiling for most people. Running Ollama, LibreChat, AnythingLLM or Hermes? Start at **$43.88/year** and don't negotiate downward.

Before you pay, confirm three things on the order page: the annual total in USD rather than the monthly equivalent, the data center you're selecting, and the renewal rate for that specific plan. RackNerd doesn't publish a money-back window on its plan pages, so treat the annual prepay as committed money and start with the cheapest plan that fits rather than the biggest one you can afford. 👉 [Start with the $11.29/year RackNerd plan](https://bit.ly/RacKnerd)
