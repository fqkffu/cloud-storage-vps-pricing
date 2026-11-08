# Cloud Storage VPS Buying Guide: What 1 TB Actually Costs, HDD or NVMe, and How to Read the Billing Term (With the Full SpinServers Plan Table)

A terabyte of cloud storage VPS costs roughly $4 a month on spinning disks and roughly $110 a month on NVMe. The tenfold gap is the first thing to understand before you open any plan table. The second is that the billing term can move the real price by 20% or more, and most plan pages don't make that obvious.

SpinServers sits outside both camps. Its KVM VPS line uses RAID-10 SSD, the biggest disk on the page is 500 GB, and the one configuration with a published starting price is **$74.00/month for 16 vCPU, 16 GB RAM and 320 GB SSD**. That's a compute VPS with a decent disk attached, not a bulk storage box. If you need several terabytes from this provider, you're really shopping their dedicated servers, not their VPS range.

Below: the full VPS lineup, what a terabyte costs across the providers that dominate this search, how contract length changes the bill, and which workloads belong on HDD versus NVMe.

> **Quick take:** if your "cloud storage VPS" is actually a 200–300 GB backup target or Nextcloud box that also needs real CPU and a 1 Gbps port, the 16 vCPU / 320 GB build at $74.00/month is the one worth pricing out. If you need 2–10 TB of cheap disk, this is the wrong shop, and the per-TB table below shows why.
> 👉 [See the SpinServers VPS lineup and current starting prices](https://bit.ly/Spinservers)

## The full SpinServers VPS lineup

Five KVM configurations, all on RAID-10 SSD with a 1 Gbps network port, one IPv4 and one IPv6 address, and between 8 TB and 20 TB of monthly transfer. Port 25 is closed on every VPS by default; opening it requires a support ticket with a justification, and they reserve the right to refuse.

| Plan | vCPU / RAM | Disk | Monthly transfer | Price | Order |
| --- | --- | --- | --- | --- | --- |
| Simple Application Server | 6 vCPU / 8 GB DDR4 | 120 GB RAID-10 SSD | 8 TB | — | [Order](https://bit.ly/Spinservers) |
| Simple Application Server | 8 vCPU / 8 GB DDR4 | 160 GB RAID-10 SSD | 10 TB | — | [Order](https://bit.ly/Spinservers) |
| KVM 12 vCPU 12 GB | 12 vCPU / 12 GB DDR4 | 160 GB RAID-10 SSD | 10 TB | — | [Order](https://bit.ly/Spinservers) |
| KVM 16 vCPU 16 GB (featured) | 16 vCPU / 16 GB DDR4 | 320 GB RAID-10 SSD | 15 TB | from $74.00/mo USD | [Order](https://bit.ly/Spinservers) |
| Advanced Application Server | 32 vCPU / 32 GB | 500 GB SSD | 20 TB | — | [Order](https://bit.ly/Spinservers) |

The 16 vCPU build is the only tier carrying a public starting price; the other four show their exact figure when you configure the order.

Read the disk column as the real constraint. 120 GB to 500 GB handles a family Nextcloud install, a PhotoPrism library of a few thousand photos, or a Borg repository for a handful of servers. It does not handle a media library measured in terabytes, and no amount of extra CPU changes that.

Where SpinServers does go past 500 GB is the dedicated line: third-party write-ups describe an enterprise-focused operation out of Dallas and Silicon Valley with 10 Gbps and 40 Gbps options and SOC 2, HIPAA and PCI compliance claims, and list an entry dedicated configuration around $49/month with a 1 TB NVMe drive and 32 GB RAM. That figure isn't on the VPS page, so confirm it at order time if a single-tenant box with a big NVMe drive is what you're after.

## What a terabyte actually costs, side by side

This is the number that decides the purchase, and it's the one plan tables usually hide behind different disk sizes. Everything below is current published pricing, converted to cost per usable TB per month.

| Provider | Disk type | Capacity at that price | Price | Cost per TB |
| --- | --- | --- | --- | --- |
| HostHatch | Enterprise HDD | 1 TB | from $5.00/mo | ≈ $5.00 |
| HostHatch | Enterprise HDD | 10 TB | from $38.00/mo | ≈ $3.80 |
| Contabo | SSD | 1.4 TB | $35.60/mo effective on a 24-month term | ≈ $25.40 |
| Cloudzy | NVMe | 240 GB | $26.48/mo (50% off) | ≈ $110.30 |
| SpinServers | RAID-10 SSD | 320 GB | $74.00/mo | ≈ $231.25 |

Judged purely on disk, SpinServers is the most expensive entry in that table by a wide margin. Judged on what else is in the box, it's the cheapest: 16 vCPU cores and 15 TB of monthly transfer for $74 is a very different product from a 1 vCPU, 1 GB RAM HostHatch storage VM with a 2.5 TB allowance. You're paying for compute and port speed, and the disk comes along.

That distinction matters because the search term "cloud storage vps" covers two unrelated purchases. One is cheap capacity: HostHatch's storage VMs are explicitly built on "large enterprise-grade spinning hard disk drives" across eight locations, and the pricing is stated as "from," so treat it as a starting point rather than a fixed quote. The other is fast disk on a general-purpose server, which is what Cloudzy sells with an NVMe-only lineup on AMD EPYC and DDR5 across 13 regions, a 40 Gbps uplink and a 14-day money-back window.

If you want the SpinServers configuration specifically rather than the cheapest disk, this is the one to price:
👉 [Price out the 16 vCPU / 320 GB build](https://bit.ly/Spinservers)

## The billing term moves the price more than the discount does

Two providers on this list advertise lower prices using completely different mechanics, and mixing them up is how people end up budgeting wrong.

Contabo shows $5.28/month on its 300 GB Storage VPS 10, but the footnote says the displayed price is the **effective monthly rate for a 24-month subscription including applicable taxes**. The standard rate is $6.60. On the 1.4 TB Storage VPS 50, it's $44.50 standard versus $35.60 effective, which over 24 months is $1,068 versus $854. Their contract terms: minimum initial term of one month, and every following term matches the initial one. Pre-paid accounts have no cancellation notice requirement because the money is already in; post-paid accounts need four weeks.

Cloudzy does the opposite. Its $3.48 and $7.48 figures are "50% off" prices with the original $6.95 and $14.95 printed next to them, and the page doesn't state what happens at renewal. If the 240 GB plan renews at the $52.95 list rate, year two costs $635.40 against $317.76 in year one.

Neither approach is dishonest, but they're not comparable at a glance. Multiply by the term before you compare: 24 months of Contabo at the effective rate, 12 months of Cloudzy at the promotional rate plus 12 at list, and whatever SpinServers quotes for the term you pick. If a provider won't tell you the renewal rate, assume the list price and budget for it.

👉 [Open the SpinServers order form to check term and billing options](https://bit.ly/Spinservers)

## HDD, SSD or NVMe: what the disk type lets you run

Contabo states plainly that its Storage VPS suits applications that "don't have high I/O requirements." Onidel, which runs its storage tier on Ceph with triple replication across HDD nodes, is more direct: HDD is fine for sequential reads and writes, and for databases they recommend their NVMe tiers instead. Cloudzy goes the other way entirely and refuses to sell HDD at all, arguing that direct-attached NVMe is faster than attached block volumes and pricing accordingly.

Practical translation:

- **Borg or restic repositories** are sequential and deduplicated. HDD is fine, and it's where the per-TB price collapses to $4–5.
- **MinIO in single-node single-drive mode** runs on one VPS and is the most common storage workload Cloudzy sees. Distributed mode needs four or more instances linked together, which changes the budget by a factor of four.
- **Nextcloud, Seafile, PhotoPrism** care about capacity first and CPU second. A 120–320 GB SSD with 8–16 cores handles a small team comfortably.
- **Databases and high-concurrency workloads** don't belong on any HDD tier, and both Contabo and Onidel say so themselves. That's what NVMe compute plans exist for.

## Two things the plan tables leave out

**Triple replication is not a backup.** Onidel replicates every block three times across separate disks and nodes and advertises 99.999999% durability, then states in its own FAQ that this protects against hardware failure, not against you deleting a file or a ransomware event, and recommends keeping your own backup strategy. Any provider selling replicated storage is making the same distinction whether they say it or not.

**Block storage usually isn't sold separately.** Cloudzy bundles the disk into the VPS and doesn't offer an EBS-style attachable volume at all. Contabo pitches its Storage VPS as a block-storage alternative for people who'd rather have a whole VM. If your architecture assumes you can grow a volume independently of the server, check that assumption before you buy anywhere.

## Which plan for which job

- **Nightly backups from a handful of servers, under 500 GB:** the SpinServers 16 vCPU / 320 GB at $74/month is more machine than the job needs, but the 1 Gbps port and 15 TB of transfer make restores fast, and you're not sharing a 1 vCPU box with anyone.
- **2 TB and up of cold archive:** buy HDD capacity. HostHatch's 10 TB tier at $38/month works out to about $3.80/TB, and Contabo's 1.4 TB SSD at $35.60 effective is the middle option if you want flash and can commit to 24 months.
- **Self-hosted S3 for an app:** capacity is almost irrelevant next to egress and port speed. A single MinIO node on a 300 GB disk stores plenty of small objects; the 1 Gbps port on a SpinServers VPS moves them out quickly.
- **Media library or photo backup:** work out the ceiling first. If you're at 800 GB today, a 500 GB plan is already too small and you should be looking at TB-scale HDD tiers, not at CPU.

## Who should skip SpinServers for this

Anyone whose primary need is cheap terabytes. At $231/TB, the VPS line can't compete with a $3.80/TB HDD storage VM, and no amount of RAM closes that gap.

Anyone who needs under 100 GB. The smallest plan here is 120 GB with 6 cores; a $5/month storage VM or an object storage bucket does that job for a tenth of the price.

Anyone running a database on the storage tier. Get NVMe compute instead, from whichever provider you prefer.

## Five checks before you pay

1. **Contract length.** One month, twelve, or twenty-four. The effective monthly rate on a 24-month term is not the price you pay if you leave early.
2. **Renewal price.** If the page shows a discount, find the list price next to it and multiply by twelve.
3. **Taxes and currency.** Contabo's headline rate includes applicable taxes; others quote before tax. Confirm at checkout.
4. **Transfer limits and fair use.** Contabo's outgoing traffic is unlimited under a fair usage policy with throttling reserved for abnormal usage; HostHatch lists hard monthly caps and notes that APAC bandwidth limits differ by region.
5. **Refund window.** Cloudzy offers 14 days; SpinServers' terms vary by product, so read them on the order page rather than assuming.

The rule of thumb: match the disk type to the workload first, then compare cost per TB inside that category, then check what the second year costs. Do it in that order and the plan table stops being a wall of numbers.

👉 [Compare all five SpinServers VPS plans](https://bit.ly/Spinservers)
