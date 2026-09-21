# BandwagonHost multi-location VPS: How Free Datacenter Migration Works, What All 47 Plans Cost, and Which Location Tier to Pick

Most VPS providers lock you into one datacenter when you order. Move means backup, cancel, re-order, restore, and a support ticket in between. BandwagonHost (often shortened to BWH, or 搬瓦工 in Chinese communities) built its service around the opposite idea: you pick a location at checkout, and you can move your VPS to another datacenter later with one click, free, without losing your data.

That sounds good on a feature list. The practical questions are messier: which locations can you actually reach from each plan? What does the same 2 GB of RAM cost in Los Angeles versus Hong Kong? And is the cheap entry plan usable at all? I went through the current plan data on the official ordering system (47 plans across 4 tiers and 11 cities) and pulled out what matters.

## What "multi-location" actually means at BandwagonHost

BandwagonHost currently operates across 11 cities, but not every plan can reach every city. This is the single most misunderstood part of the product. The order system sorts everything into four product tiers, and each tier has its own location map.

| City | Datacenter | Available tiers | Network highlights |
| --- | --- | --- | --- |
| Los Angeles, US | USCA_2 (Coresite LA2) | Basic, E-Commerce | ChinaNet / Unicom / Mobile peering |
| Los Angeles, US | USCA_9 (Coresite LA2) | E-Commerce | CN2 GIA + CMIN2 + Unicom Premium, AMD+NVMe |
| Los Angeles, US | USCA_5 (Coresite LA2) | E-Commerce+SLA | CN2 GIA, 99.99% SLA, dual-redundant fabric |
| Los Angeles, US | USCA_6 (Digital Realty LAX10) | E-Commerce | CN2 GIA + CMIN2 + Unicom Premium |
| Fremont, US | USCA_FMT (Hurricane fmt2) | Basic, E-Commerce | Hurricane Electric, local peering |
| San Jose, US | USCA_SJC5 (Equinix SV10) | E-Commerce | CN2 GIA + CMIN2 + Unicom Premium |
| New York, US | USNY_6 (Coresite NY1) | Basic, E-Commerce | Manhattan, DECIX, Google/Facebook peering |
| New York, US | USNY_8 (Coresite NY1) | E-Commerce | CN2 GIA + CMIN2 + Unicom Premium |
| Vancouver, CA | CABC_1 (Cologix VAN3) | Basic, E-Commerce | Local/Canadian peering |
| Vancouver, CA | CABC_6 (Cologix VAN3) | E-Commerce | CN2 GIA + CMIN2 + Unicom Premium |
| Amsterdam, NL | EUNL_2 (Iron Mountain) | Basic, E-Commerce | Arelion, NL-IX, local peering |
| Amsterdam, NL | EUNL_1 (Iron Mountain) | E-Commerce | CTGNet + CMIN2 + Unicom Premium, AMD+NVMe |
| Amsterdam, NL | EUNL_9 (Iron Mountain) | E-Commerce | China Unicom Premium peering |
| Dubai, UAE | AEDXB_1 (Equinix DX1) | E-Commerce (Dubai plans) | Direct DU and Etisalat peering |
| Osaka, JP | JPOS_1 (Equinix OS1) | E-Commerce | Softbank, NTT peering |
| Osaka, JP | JPOS_6 (Equinix OS1) | Ultra | CN2 GIA peering |
| Tokyo, JP | JPTY_1 (Equinix TY8) | E-Commerce | Softbank, "China Direct" |
| Tokyo, JP | JPTY_8 (Equinix TY8) | Ultra | CN2 GIA peering |
| Hong Kong | HK_8 (Equinix HK2) | Ultra | CN2 GIA, Equinix IX, China Mobile |
| Singapore | SG_8 (Equinix SG1) | Ultra | CN2 GIA + CMIN2 |

Two things worth noticing. The densest cluster is on the US West Coast, which is where the China-facing network engineering happens. And the premium locations (Hong Kong, Tokyo, Osaka, Singapore) exist only in the top tier — you can't buy a $49.99/year plan and end up in Hong Kong, no matter how much you'd like to.

## The four tiers, in plain terms

**Basic VPS** is the budget line. Six plans, five datacenters (Los Angeles, Fremont, New York, Vancouver, Amsterdam), local peering only. This is for generic workloads — a personal site, a dev box, a small proxy — where route quality to China is irrelevant.

**E-Commerce VPS** is the middle tier and, honestly, the one most people searching for multi-location hosting want. The plans here can land in 15 datacenters, including every CN2 GIA-equipped US site, Osaka, Tokyo, Dubai, and all three Amsterdam locations. Migration within the tier is free and instant.

**E-Commerce+SLA** is a newer Los Angeles-only variant hosted in USCA_5. Same idea as E-Commerce, but with a 99.99% uptime Service Level Agreement, dual redundant edge routers, and certifications like ISO 27001 and PCI DSS on the facility. Only six plans exist, and only one location is available.

**Ultra VPS** is the premium Asia tier: Hong Kong (Equinix HK2), Tokyo (Equinix TY8), and Osaka (Equinix OS6) on CN2 GIA routes, plus Singapore. Spec-for-spec it costs 5–10x what the E-Commerce line costs. You're paying for latency, not hardware.

## Full plan and price list (all currently listed plans)

All prices are USD, straight from the current official ordering data. Traffic is monthly, and every plan is unmanaged KVM with full root access.

### Basic VPS (5 locations)

| Plan | CPU | RAM | SSD | Traffic | Port | From | Order |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 20G KVM PROMO | 2x | 1 GB | 20 GB | 1 TB | 1 Gbps | $49.99/yr | [ Order 20G Basic](https://bandwagonhost.com/aff.php?aff=79616&pid=44) |
| 40G KVM PROMO | 3x | 2 GB | 40 GB | 2 TB | 1 Gbps | $99.99/yr ($52.99/6mo) | [ Order 40G Basic](https://bandwagonhost.com/aff.php?aff=79616&pid=45) |
| 80G KVM PROMO | 4x | 4 GB | 80 GB | 3 TB | 1 Gbps | $19.99/mo or $199.99/yr | [ Order 80G Basic](https://bandwagonhost.com/aff.php?aff=79616&pid=46) |
| 160G KVM PROMO | 5x | 8 GB | 160 GB | 4 TB | 1 Gbps | $39.99/mo or $399.99/yr | [ Order 160G Basic](https://bandwagonhost.com/aff.php?aff=79616&pid=47) |
| 320G KVM PROMO | 6x | 16 GB | 320 GB | 5 TB | 1 Gbps | $79.99/mo or $799.99/yr | [ Order 320G Basic](https://bandwagonhost.com/aff.php?aff=79616&pid=48) |
| 480G KVM PROMO | 7x | 24 GB | 480 GB | 6 TB | 1 Gbps | $119.99/mo or $1,199.99/yr | [ Order 480G Basic](https://bandwagonhost.com/aff.php?aff=79616&pid=49) |

The 20G plan's $49.99/year price only exists on the annual cycle. If you want to pay monthly, the smallest option is the 80G plan at $19.99. That catches a lot of people off guard.

### E-Commerce VPS — CN2 GIA-E (15 locations)

| Plan | CPU | RAM | SSD | Traffic | Port | From | Order |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 20G CN2 GIA-E | 2x | 1 GB | 20 GB | 1 TB | 2.5 Gbps | $169.99/yr ($49.99/q) | [ Order 20G GIA-E](https://bandwagonhost.com/aff.php?aff=79616&pid=87) |
| 40G CN2 GIA-E | 3x | 2 GB | 40 GB | 2 TB | 2.5 Gbps | $299.99/yr ($89.99/q) | [ Order 40G GIA-E](https://bandwagonhost.com/aff.php?aff=79616&pid=88) |
| 80G CN2 GIA-E | 4x | 4 GB | 80 GB | 3 TB | 2.5 Gbps | $56.99/mo or $549.99/yr | [ Order 80G GIA-E](https://bandwagonhost.com/aff.php?aff=79616&pid=89) |
| 160G CN2 GIA-E | 6x | 8 GB | 160 GB | 5 TB | 5 Gbps | $86.99/mo or $879.99/yr | [ Order 160G GIA-E](https://bandwagonhost.com/aff.php?aff=79616&pid=90) |
| 320G CN2 GIA-E | 8x | 16 GB | 320 GB | 8 TB | 5 Gbps | $159.99/mo or $1,599.99/yr | [ Order 320G GIA-E](https://bandwagonhost.com/aff.php?aff=79616&pid=91) |
| 640G CN2 GIA-E | 10x | 32 GB | 640 GB | 10 TB | 10 Gbps | $289.99/mo or $2,759.99/yr | [ Order 640G GIA-E](https://bandwagonhost.com/aff.php?aff=79616&pid=92) |
| 1280G CN2 GIA-E | 12x | 64 GB | 1.28 TB | 12 TB | 10 Gbps | $549.99/mo or $5,499.99/yr | [ Order 1280G GIA-E](https://bandwagonhost.com/aff.php?aff=79616&pid=93) |
| 1280G GIA-E HIBW 15T | 12x | 64 GB | 1.28 TB | 15 TB | 10 Gbps | $679.00/yr | [ Order 1280G HIBW 15T](https://bandwagonhost.com/aff.php?aff=79616&pid=160) |
| 1280G GIA-E HIBW 20T | 12x | 64 GB | 1.28 TB | 20 TB | 10 Gbps | $899.90/yr | [ Order 1280G HIBW 20T](https://bandwagonhost.com/aff.php?aff=79616&pid=161) |

The two HIBW (high bandwidth) variants are interesting: they take the flagship 12-core plan and swap some of the absurd CPU count for three to five times the traffic allowance, at a much lower annual price than the 12 TB original. If your workload is bandwidth-heavy rather than compute-heavy, they're the better buy of the three.

### E-Commerce+SLA (Los Angeles USCA_5 only, 99.99% SLA)

| Plan | CPU | RAM | SSD | Traffic | Port | From | Order |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 20G SLA | 2x | 1 GB | 20 GB | 1 TB | 2.5 Gbps | $239.99/yr ($65.89/q) | [ Order 20G SLA](https://bandwagonhost.com/aff.php?aff=79616&pid=164) |
| 40G SLA | 3x | 2 GB | 40 GB | 2 TB | 2.5 Gbps | $399.99/yr ($116.99/q) | [ Order 40G SLA](https://bandwagonhost.com/aff.php?aff=79616&pid=165) |
| 80G SLA | 4x | 4 GB | 80 GB | 3 TB | 2.5 Gbps | $69.99/mo or $699.99/yr | [ Order 80G SLA](https://bandwagonhost.com/aff.php?aff=79616&pid=166) |
| 160G SLA | 6x | 8 GB | 160 GB | 5 TB | 5 Gbps | $109.99/mo or $1,099.99/yr | [ Order 160G SLA](https://bandwagonhost.com/aff.php?aff=79616&pid=167) |
| 320G SLA | 8x | 16 GB | 320 GB | 8 TB | 5 Gbps | $199.99/mo or $1,999.99/yr | [ Order 320G SLA](https://bandwagonhost.com/aff.php?aff=79616&pid=168) |
| 640G SLA | 10x | 32 GB | 640 GB | 10 TB | 10 Gbps | $369.99/mo | [ Order 640G SLA](https://bandwagonhost.com/aff.php?aff=79616&pid=169) |

The SLA tier costs roughly 40% more than the equivalent E-Commerce plan. Whether that premium is worth it depends entirely on how much an hour of downtime costs you. For a storefront doing real revenue, $70/year extra on the 80G plan is cheap insurance. For a hobby project, it isn't.

### Ultra VPS — Hong Kong, Tokyo, Osaka (CN2 GIA)

| Plan (per location) | CPU | RAM | SSD | Traffic | Hong Kong / Tokyo | Osaka | Order |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 40G Ultra | 2x | 2 GB | 40 GB | 500 GB | $89.99/mo · $899.99/yr | $49.99/mo · $499.99/yr | [ HK](https://bandwagonhost.com/aff.php?aff=79616&pid=95) · [ TYO](https://bandwagonhost.com/aff.php?aff=79616&pid=108) · [ OSA](https://bandwagonhost.com/aff.php?aff=79616&pid=134) |
| 80G Ultra | 4x | 4 GB | 80 GB | 1 TB | $155.99/mo · $1,559.99/yr | $86.99/mo · $869.99/yr | [ HK](https://bandwagonhost.com/aff.php?aff=79616&pid=96) · [ TYO](https://bandwagonhost.com/aff.php?aff=79616&pid=109) · [ OSA](https://bandwagonhost.com/aff.php?aff=79616&pid=135) |
| 160G Ultra | 6x | 8 GB | 160 GB | 2 TB | $299.99/mo · $2,999.99/yr | $165.99/mo · $1,665.99/yr | [ HK](https://bandwagonhost.com/aff.php?aff=79616&pid=97) · [ TYO](https://bandwagonhost.com/aff.php?aff=79616&pid=110) · [ OSA](https://bandwagonhost.com/aff.php?aff=79616&pid=136) |
| 320G Ultra | 8x | 16 GB | 320 GB | 4 TB | $589.99/mo · $5,899.99/yr | $329.99/mo · $3,199.00/yr | [ HK](https://bandwagonhost.com/aff.php?aff=79616&pid=98) · [ TYO](https://bandwagonhost.com/aff.php?aff=79616&pid=111) · [ OSA](https://bandwagonhost.com/aff.php?aff=79616&pid=137) |
| 640G Ultra | 10x | 32 GB | 640 GB | 6 TB | $989.99/mo · $9,989.99/yr | $549.99/mo · $5,549.99/yr | [ HK](https://bandwagonhost.com/aff.php?aff=79616&pid=122) · [ TYO](https://bandwagonhost.com/aff.php?aff=79616&pid=123) · [ OSA](https://bandwagonhost.com/aff.php?aff=79616&pid=138) |
| 1280G Ultra | 12x | 64 GB | 1.28 TB | 8 TB | $1,889.99/mo · $18,989.99/yr | $1,059.99/mo · $10,559.99/yr | [ HK](https://bandwagonhost.com/aff.php?aff=79616&pid=124) · [ TYO](https://bandwagonhost.com/aff.php?aff=79616&pid=125) · [ OSA](https://bandwagonhost.com/aff.php?aff=79616&pid=139) |

Osaka runs noticeably cheaper than Hong Kong and Tokyo at identical specs, and its hardware allocation is more generous relative to price. If you want Asia-Pacific CN2 GIA without the HK premium, Osaka deserves a look first. Note the traffic allowance drops sharply at this tier — the HK 40G plan gets 500 GB/month, versus 1 TB on a Basic plan that costs a twelfth as much.

### Dubai VPS (Equinix DX1)

| Plan | CPU | RAM | SSD | Traffic | Port | Price | Order |
| --- | --- | --- | --- | --- | --- | --- | --- |
| DUBAI 20G | 2x | 1 GB | 20 GB | 500 GB | 1 Gbps | $19.99/mo | [ Order Dubai 20G](https://bandwagonhost.com/aff.php?aff=79616&pid=114) |
| DUBAI 40G | 3x | 2 GB | 40 GB | 1 TB | 1 Gbps | $32.99/mo | [ Order Dubai 40G](https://bandwagonhost.com/aff.php?aff=79616&pid=115) |
| DUBAI 80G | 4x | 4 GB | 80 GB | 2 TB | 1 Gbps | $56.99/mo | [ Order Dubai 80G](https://bandwagonhost.com/aff.php?aff=79616&pid=116) |
| DUBAI 160G | 6x | 8 GB | 160 GB | 3 TB | 1 Gbps | $86.99/mo | [ Order Dubai 160G](https://bandwagonhost.com/aff.php?aff=79616&pid=117) |

Dubai is a niche play: direct peering with DU and Etisalat makes it genuinely useful for UAE audiences, and BandwagonHost points out that most local VPS offerings there ship with 5–10 Mbps uplinks while these plans get the full gigabit. The Dubai line also includes free automatic backups, which the standard plans don't advertise as a bundled feature.

## The migration feature, and why it changes how you should buy

Here's the workflow that distinguishes this provider. Inside your tier, you open the KiwiVM control panel, pick a different datacenter, and the VPS migrates over with all data intact. No reinstall, no snapshot shuffling, no charge. The company states this plainly on every order page: VPS can be migrated between locations anytime, free of charge, without data loss.

The strategic consequence: you don't have to guess the right location on day one. A reasonable pattern is to start a CN2 GIA-E plan in Los Angeles (the cheapest tier entry point with the widest location list), watch your actual route performance for a few weeks, then move to Osaka, San Jose, or New York if the data says so. That's a very different decision calculus than most hosts force on you, where the location you pick at checkout is the location you keep.

One boundary to respect: migration stays within the tier's own location map. A Basic plan can move among its five datacenters; it cannot jump to Hong Kong. Tier changes aren't a one-click migration.

## CN2 GIA, briefly, for people who don't care about networking jargon

If your visitors aren't in mainland China, skip this section — any Basic plan will serve you fine. If they are, here's the short version from BandwagonHost's own network documentation: ordinary transit routes into China (ChinaNet/163, and even the mid-tier CN2 GT) get congested during peak hours, with packet loss that can reach 30% or more. At that level, web pages load slowly, video calls stutter, and game connections fall apart. CN2 GIA is China Telecom's premium class of transit — stable where the cheap routes aren't — and CTGNet is its practically equivalent newer sibling.

The trade-offs are real. CN2 GIA capacity is scarce and expensive (the company cites transit prices up to $120 per megabit), and the network doesn't absorb DDoS attacks well — under attack, the affected IP gets null-routed rather than filtered. So it's the right tool for serving content to China, and the wrong tool for anything that expects to be attacked.

This is also why the E-Commerce tier is the sweet spot for most China-facing users: USCA_9 in Los Angeles sends China-bound traffic over CN2 GIA (AS4809), China Unicom Premium (AS10099), and China Mobile CMIN2 (AS58807) simultaneously, with direct peering to Google, Apple, Facebook, and Bytedance — at a quarter of what the Ultra tier charges.

## Limits and fine print worth knowing before ordering

A few things the plan tables won't tell you:

- **Everything is self-managed.** No control-file support, no hand-holding. If you can't run a Linux server yourself, this isn't the right product regardless of location.
- **Refunds have conditions.** There's a 30-day money-back guarantee, but it's governed by the terms of service and applies to properly requested, eligible orders — don't treat it as an unconditional trial.
- **Prohibited uses are explicit.** The terms of service ban Tor relays and exit nodes, adult content, spam, data mining/crawling abuse, and similar categories. People shopping for a VPN endpoint should read the AUP first.
- **RAM sizes on SLA plans are slightly odd** (1,060 MB, 2,092 MB, and so on) because of the SLA overhead allocation — cosmetic, but don't be surprised when the panel shows 1.03 GB.
- **Promo codes are episodic.** BandwagonHost runs sitewide recurring discount codes around events like Black Friday and its anniversary, but there's no permanent universal code displayed on the official site right now. Anything promising a standing "2026 discount code" outside the official site should be treated skeptically — and note that the entry prices worth having (the $49.99/year Basic and $169.99/year GIA-E annual rates) are already the listed prices.

## Which plan fits which situation

Based on the pricing above, some honest routing:

- **Generic VPS needs, zero China requirements:** 20G Basic at $49.99/year in Fremont or Amsterdam. Hard to beat on cheap annual KVM.
- **Website or app with Chinese visitors, small team budget:** 20G CN2 GIA-E at $169.99/year, start in Los Angeles USCA_9, migrate later if needed. This is the plan most people searching for multi-location BWH hosting actually want.
- **Production e-commerce where uptime is revenue:** the SLA tier, 80G at $699.99/year, for the 99.99% commitment and redundant fabric.
- **Latency-sensitive China connectivity, budget is secondary:** Osaka Ultra — half the price of the identical Hong Kong plan.
- **Gulf-region audience:** Dubai 20G at $19.99/month with the full gigabit port.

If you want to browse the tiers side by side before committing, you can [👉 view all plans and locations on the official order page](https://bit.ly/BandwagonHost). The location picker there shows the same datacenter map reflected above, tier by tier.

## Frequently asked questions

**Can I change datacenter after purchase?**
Yes, within your tier's location list, via KiwiVM, free, without data loss. The feature is the core of the multi-location pitch.

**Do all plans come with the same locations?**
No. Basic has 5 locations, E-Commerce has 15, SLA is Los Angeles only, and Ultra is limited to Hong Kong, Tokyo, Osaka, and Singapore.

**Is there a cheaper monthly option than $19.99?**
Not on the current lineup. The $49.99/year Basic plan is annual-only; monthly billing starts with the 80G plans.

**What's the difference between CN2 GIA-E and the Hong Kong plans?**
GIA-E plans are US/EU/Japan machines with premium China-bound routing added on top. The Hong Kong/Tokyo/Osaka Ultra plans are physically located in Asia, so latency is far lower — that proximity is what you're paying the 5–10x premium for.

**Which OS can I install?**
AlmaLinux, RockyLinux, CentOS, CentOS Stream, Debian, Ubuntu, and Fedora from templates, plus bootable ISOs on request, all managed through the KiwiVM panel with full root access.
