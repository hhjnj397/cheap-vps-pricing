# Buy Cheap VPS: Is $2 a Month Enough, What Do 16 Cores at $74 Get You, and Which Add-Ons Double the Bill? (Plan Table + Renewal Checklist)

A cheap VPS starts at $2 a month, and most plans people actually buy land between $4 and $100, quoted on first-term or annual billing in the list prices we checked in October 2026. Two numbers decide whether it stays cheap: the renewal price, and what the host charges on top for backups and a control panel. Get either wrong and a $4.99 plan ends up costing more than a $12 one.

Below: what the entry price really buys, where a high-core plan like SpinServers' 16 vCPU / 16 GB at $74.00 a month beats stacking up budget boxes, the add-ons that quietly raise the bill, and how much traffic each spec tier actually carries.

> **Short version.** 1 vCPU with 1 GB RAM is a test box. A small WordPress site needs 2 GB RAM and 20–50 GB of SSD or NVMe. WooCommerce or several sites at once starts at 4 GB. Budget $4–$10 at first-term pricing and check the renewal before you commit.
>
> If what you need is cores and transfer rather than a $2 test box, SpinServers lists KVM plans from 6 to 32 vCPU with 8 to 20 TB of monthly bandwidth, and the 16 vCPU / 16 GB / 320 GB plan is $74.00 a month. 👉 [See SpinServers' KVM VPS plans and current pricing](https://bit.ly/Spinservers)

## What $2 a month actually buys right now

$2 is the floor of the market, not the middle. IONOS lists plans from $2 a month, Vultr from $2.50, Netcup from €3.35 for 2 vCore / 2 GB RAM / 64 GB SSD, Hetzner Cloud from €4.35, and DigitalOcean from $4. At those prices you're buying a slice of one physical machine, 10 to 50 GB of storage, one IPv4 address and roughly 1 TB of monthly transfer.

| Provider | Listed from | Billing basis | Range as listed | What to watch |
| --- | --- | --- | --- | --- |
| IONOS | $2/mo | Monthly | 1–24 GB RAM, 10–640 GB SSD | Backups cost extra, limited data centre choice |
| Vultr | $2.50/mo | Monthly | SSD instances, specs scale by plan | Entry tier is test-grade |
| Netcup | €3.35/mo | Monthly | 2 GB RAM, 64 GB SSD at entry | EUR billing, Europe-focused |
| DigitalOcean | $4/mo | Monthly | 512 MiB–256 GiB RAM, 10 GiB–4,690 GiB SSD | No refunds |
| Hetzner Cloud | €4.35/mo | Monthly | NVMe storage, AMD EPYC | EUR billing, regions in Germany, Finland and the US |
| Hostinger | $4.99/mo | First 24 months | 4 GB RAM, 50 GB NVMe at entry | No Windows VPS, no managed service |
| Hostwinds | $4.99/mo | First billing cycle | 1–96 GB RAM, 30–750 GB SSD | 3-day return window, SSL not included |
| OVHcloud | ~$5/mo | Monthly | Unlimited traffic up to 500 Mbps | Specs vary by region |

Every price in that table is a published list price, not a renewal quote, and several are explicitly tied to a first term. The top of the market is far away from this: DigitalOcean's range runs to $2,096 a month.

## Where SpinServers fits in a "cheap VPS" search

SpinServers isn't a $2 host. Its KVM VPS page starts at 6 vCPU and goes to 32, and the specs are built around cores, RAM and monthly transfer rather than the smallest possible invoice. Five plans are listed:

| Plan | vCPU / RAM | Storage | Monthly transfer | Listed price | Order |
| --- | --- | --- | --- | --- | --- |
| KVM 6 vCPU / 8 GB | 6 / 8 GB DDR4 | 120 GB RAID-10 SSD | 8 TB | Not shown on the page | [View plan](https://bit.ly/Spinservers) |
| KVM 8 vCPU / 8 GB | 8 / 8 GB DDR4 | 160 GB RAID-10 SSD | 10 TB | Not shown on the page | [View plan](https://bit.ly/Spinservers) |
| KVM 12 vCPU / 12 GB | 12 / 12 GB DDR4 | 160 GB RAID-10 SSD | 10 TB | Not shown on the page | [View plan](https://bit.ly/Spinservers) |
| KVM 16 vCPU / 16 GB | 16 / 16 GB DDR4 | 320 GB RAID-10 SSD | 15 TB | **$74.00/mo** | [View plan](https://bit.ly/Spinservers) |
| KVM 32 vCPU / 32 GB | 32 / 32 GB | 500 GB SSD | 20 TB | Not shown on the page | [View plan](https://bit.ly/Spinservers) |

All five include a 1 Gbps network port and one IPv4 plus one IPv6 address. Only the 16 vCPU model carries a public price on that page; the other four are spec-only, so ask for a quote before you treat them as comparable to anything else in this article.

The arithmetic on the one priced plan is the interesting part. $74.00 ÷ 16 vCPU works out to about $4.63 per vCPU, with 1 GB of RAM per core and roughly 940 GB of transfer per core. A $4.99 budget VPS gives you one vCPU and 1–4 GB of RAM for that same $4.99. If your workload is CPU-bound (build servers, containers, batch jobs, log processing), paying per core is the number that matters, and this is where the per-core maths starts to look reasonable. If your workload is one small website, it's irrelevant, and you should stay in the table above.

Two details before you buy:

- **Port 25 is closed by default on every VPS.** You can open a ticket with a justification and they reserve the right to refuse. If your plan involves sending mail straight from the server, plan for an external SMTP relay instead.
- **No money-back window is advertised for month-to-month service.** Reviews of the provider note that month-to-month orders generally aren't refundable, so treat the first invoice as final and do your testing in week one. The provider does list a 99.99% uptime SLA, support by ticket, phone and email, and cPanel or Plesk as control panel options.

One boundary worth knowing: dedicated hardware from SpinServers starts at $79 a month for an Intel Xeon E3-1280 v5 with 32 GB RAM, 1 TB NVMe and 30 TB of transfer in Dallas or San Jose. That's $5 more than the 16 vCPU VPS, with half the cores and four times the RAM and storage. If RAM is your bottleneck rather than core count, the entry dedicated box is the better buy. 👉 [Compare SpinServers' VPS and dedicated options](https://bit.ly/Spinservers)

## The real spec floor for a budget VPS

Cheap plans converge on the same shape. This is what the money buys and what breaks first:

| Component | What cheap plans give | What to check |
| --- | --- | --- |
| vCPU | 1 vCPU at entry, 2 vCPU for a growing site | More cores help with dynamic sites and background jobs |
| RAM | 1 GB for testing, 2 GB for a small WordPress site, 4 GB+ for WooCommerce or multiple sites | RAM decides whether the panel, database and PHP survive together |
| Storage | 20–50 GB SSD or NVMe | NVMe is faster than SATA SSD; capacity and speed vary a lot |
| Bandwidth | Around 1 TB/month is common | Fair-use clauses and overage fees hide in the terms |
| Root access | Usually included on unmanaged plans | Root means you own the maintenance too |
| OS | Ubuntu, Debian, AlmaLinux, Rocky Linux; Windows often costs extra | Confirm the image you need exists before ordering |
| Dedicated IP | Usually one IPv4 included | Extra IPv4 addresses are a paid add-on |
| Backups | Sometimes included, often an add-on | Check whether backups are automatic or manual |
| Control panel | Custom panels may be free; cPanel, Plesk and DirectAdmin usually cost extra | A panel can double the effective monthly price |

The 1 GB rule is worth stating plainly: 1 GB is for testing, a staging box, a tiny static site or a VPN endpoint. It is not enough to run WooCommerce, and it's tight for WordPress with a few plugins once the database grows.

## The hidden costs that turn $4.99 into $15

Nine line items show up on budget VPS bills, and almost none of them are in the headline price:

1. **Control panel fees.** cPanel, Plesk and DirectAdmin are usually licensed separately. Entry plans that bundle cPanel tend to sit around $8–$10 a month with thin resources.
2. **Backup fees.** Automated backups and snapshots are frequently add-ons.
3. **Extra IPv4 addresses.** One is normally included, additional ones are billed.
4. **Renewal price increases.** Introductory pricing expires.
5. **Managed support.** Unmanaged is cheaper only if your time is free.
6. **Migration fees.** Some hosts charge to move your data in.
7. **Security add-ons.** Malware scanning and advanced DDoS protection may be paid extras.
8. **Bandwidth limits.** Fair-use rules and overage charges.
9. **Monitoring.** Advanced monitoring often isn't in the cheap tier.

The renewal item is the one that bites hardest, and the pricing language tells you so. Hostinger's $4.99–$19.99 is "for the first 24 months". Hostwinds' $4.99–$431.24 is "during the first billing cycle". GoDaddy's $8.99–$44.99 is "for the first three years". Each of those phrases is a warning that the number you see today is not the number you'll pay later. Before you order, add up: plan price + backups + panel + any extra IP, then ask what that total becomes at renewal.

## Will the specs hold your traffic?

Sites-per-server and visits-per-month are two different measurements, and budget hosts rarely publish either. Here's a working mapping:

| Plan size | Lightweight sites it can host | Monthly visits it can carry |
| --- | --- | --- |
| 1–2 GB RAM, 1 core | 5–10 | 10,000–50,000 |
| 4–8 GB RAM, 2–4 cores | 20–50 | 100,000–500,000 |
| 16 GB+ RAM, multiple cores | 50+ | 1,000,000+ |

Caching, a CDN and database tuning push those numbers up; an unoptimised WooCommerce store with 2,000 products pulls them down.

There's also a threshold on the other side. Around 90,000 monthly visits is the point where moving off shared hosting to a VPS starts to pay for itself. Below that, if you don't know your way around Linux and the site isn't business-critical, a VPS buys you a maintenance job rather than performance.

## VPS or cloud, in one table

|  | VPS | Cloud |
| --- | --- | --- |
| Infrastructure | One physical server, split into virtual machines | A pool of servers |
| Scaling | Manual upgrade | Automatic on many plans |
| Pricing | Fixed for the resources you pick | Scales with usage |
| Failure mode | The physical host is a single point of failure | Redundancy across machines |

At $5 a month you're buying a fixed slice of one machine and a bill you can predict. Cloud pricing at the low end is metered, which is fine until a traffic spike arrives in the same week as the invoice.

## Pick by what you're running

| Your situation | Spec you need | Where to look |
| --- | --- | --- |
| Testing, learning Linux, a VPN or a tiny static site | 1 vCPU, 1 GB RAM, cheapest plan | Any entry tier in the first table |
| A small WordPress site | 2 GB+ RAM, NVMe, backups, panel | $4–$10 first-term tier |
| WooCommerce or several sites | 4 GB+ RAM, managed or semi-managed, backups | Mid tier, budget for the panel |
| Development with root and snapshots | Unmanaged, SSH, OS choice | Unmanaged plans |
| European traffic | EU data centre, low latency | Providers with EU regions |
| Email in the plan | Port 25 must be open | Confirm in writing, or use an external relay |
| 6–32 vCPU and 8–20 TB of transfer | High-core KVM | SpinServers' KVM line |
| More RAM than cores | Dedicated hardware | SpinServers' entry dedicated box at $79/mo |

## Refund windows differ more than prices do

This is the part buyers skip, and it's the part that costs money when a plan turns out to be wrong:

- **Hostinger:** 30-day money-back guarantee.
- **IONOS:** 30 days.
- **Kamatera:** 30-day trial worth up to $100 in resources.
- **Hostwinds:** 3-day return policy. Three days is not enough time to migrate a live site and test it.
- **DigitalOcean:** no refunds.
- **SpinServers:** no advertised money-back window on month-to-month service.

Free options exist and are worth naming only so you don't mistake them for hosting: Mikr.us offers an always-free micro VPS with 256 MB RAM and 3 GB storage, and DigitalOcean gives students, educators and researchers $100 in credit. Both are for experimentation. Free tiers cap CPU, storage, throughput and support, and none of them belong in front of paying customers.

## Three questions that come up before checkout

**Is a $2 VPS enough for a website?** For a static page or a personal test site, yes. For WordPress with plugins, no. The database and PHP processes alone will push a 1 GB box into swap.

**How much RAM does WooCommerce need?** Start at 4 GB. A store with a large catalogue, several plugins and concurrent checkout traffic will use it, and 2 GB leaves no headroom for a traffic spike.

**Do I need managed hosting?** If you can't comfortably work in SSH, yes. Managed costs more per month and saves you the evening you'd otherwise spend recovering a broken update.

## Before you pay

Match the plan to the job first: a test box needs 1 GB and the lowest price you can find; a small WordPress site needs 2 GB and NVMe; a store needs 4 GB and backups; a CPU-heavy workload needs cores, which is where a plan like SpinServers' 16 vCPU at $74.00 with 15 TB of transfer changes the per-core maths.

Then confirm four things in writing: the renewal price after the intro term ends, whether backups and a control panel are included, the refund window in days, and which data centre your server will sit in. Test uptime, response time and disk performance in the first week, while a refund is still theoretically possible.

👉 [Check SpinServers' KVM VPS plans and pricing before you decide](https://bit.ly/Spinservers)
