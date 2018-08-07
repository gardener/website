---
title: New Gardener Landscape Coming soon
type: Blog
---

Dear Kubernetes Gardener users,
 
This is **heads-up information about new Gardener Landscapes** that will be coming soon and the **de-continuation of the 
former self-service Gardener landscape.**
 
{{% blog_img "logo" "blog-new-landscape.svg" %}}
 
## What’s happening right now?
Actually, since the beginning of this year we are building the promised day-2 operations and have started to set 
up proper dev+staging+canary+live landscapes (automated) throughout the world with AWS accounts, Azure subscriptions, 
GCP projects, and OpenStack (SOC7) tenants all owned by us (no longer shared, i.e. fully separated and isolated), with 
proper ondemand.com domains, with self-controlled DNS (we have zone delegation to Route53) and properly signed 
certificates (by DigiCert). Consequently, you haven’t seen any new features on the self-service Gardener landscape 
you are using for long.
 
## What will happen soon?
We are now in the process of creating the remaining canary and live landscapes and will hopefully complete this 
task in April and roll out canary to you then (fyi: live is the landscape for the “indirect shipment” launched at 
Sapphire). This (new) canary landscape means, you have to recreate your projects and clusters in the new landscape 
as we won’t migrate either. If you are interested in taking over your project, you can let us know and we will 
consider it if there is sufficient interest, but we can’t migrate your clusters for various reasons.
 
## What’s in for you:
The new landscapes will bring the following features:
- AWS, Azure, GCP, and OpenStack (SAP Cloud Platform on Converged Cloud Industry Edition, SOC7)
- Latest Kubernetes v1.10
- Trial quota if you don’t own an account (clusters will self-terminate after one week)
- Modification of a cluster after creation (add, remove or modify worker pools and more, but at first only in yaml)
- Hibernation and wake-up of clusters (useful for dev clusters over night/weekend, but at first only in yaml)
- Flexible API server configuration (e.g. to activate Kubernetes alpha/beta features, but at first only in yaml)
- Automated cluster updates (the real deal for you and us as this brings a ton of flexibility)
  - Continuous reconciliation (desired vs. actual cluster state)
  - Seamless feature and bug fix roll-outs (at any time)
  - CoreOS Container Linux roll-outs (during maintenance time window)
  - Kubernetes patch version roll-outs (during maintenance time window or on-demand)
  - Kubernetes minor version roll-outs (on-demand)
  - Maintenance time window start time can be defined by you (initial proposal randomized to spread the load)
 
These are the real target landscapes and we have no plans to create new/different landscapes in the future 
(unless of course we need to comply with new requirements, but we built up these landscapes to the best of 8+ 
years Neo and 3+ years Cloud Foundry knowledge and based on the process requirements we were aware of).
 
Internally, many more things have improved (more stable and simplified etcd setup, better etcd backup & restore, 
control plane monitoring and logging, improved ops issue handling), but this has no direct impact on you. 

**However, just so that everybody is on the same page, we still lack disaster recovery and will work on it in the second 
half of 2018!**
 
**Cheers, Vedran**
 
<style>

@keyframes float {
	0% {
		transform: translatey(0);
	}
	50% {
		transform: translatey(-6px);
	}
	100% {
		transform: translatey(0);
	}
}

#blog-new-landscape #Icon > *{
animation: float 3s ease-in-out infinite;
}

</style>